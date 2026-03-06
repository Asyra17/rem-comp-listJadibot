const { Client } = require('whatsapp-web.js');

const client = new Client();

client.on('qr', (qr) => {
  // Tampilkan QR code untuk scan
  console.log('Scan QR code:', qr);
});

client.on('ready', () => {
  console.log('Bot siap!');
});

client.on('message', (message) => {
  if (message.body === 'halo') {
    message.reply('Halo juga!');
  }
});

client.initialize();
