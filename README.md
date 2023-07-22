let {Module} = require('../main');
/*
Credit: Lynxezra0
 Module({
pattern: 'forallbio ?(.*)',
fromMe: false
*/
let on_aano = false
Module({on:"text",fromMe:false},async (m)=>{
if (on_aano=== true || on_aano === null) return;
if (m.message.toLowerCase() == "autobio off") {
on_aano = null
clearInterval(bioSetter)
await m.send("_Autobio disabled. Remove plugin for completing removal process!_")
}
on_aano = true
async function setAbout(){
let status ="❤️Its joseph 🔥[🇰🇪KE⛟ "+new Date().toLocaleTimeString('en-US', { timeZone: 'Africa/Nairobi'})+"🇰🇪]××, ["+new Date().toLocaleString('en-US', { weekday: 'long', timeZone: 'Africa/Nairobi'})+"] 🔥❤️ I'm_not_here to_impress_anyone.jose_tech❤️🔥"
await m.client.updateProfileStatus(status)
return "Done"
}
m.jid = m.client.user.id
await m.send("_Jose auto bio iko poa😝!_");
let bioSetter = setInterval(setAbout,10000)
})
