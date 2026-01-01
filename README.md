const express = require('express');
const app = express();
const port = 3000;

app.use(express.json());
app.use(express.static('public'));

app.post('/request-service', (req, res) => {
  const serviceRequest = req.body;

  // Here, you can store the request in the database or perform additional processing
  res.json({ message: 'تم إرسال طلبك بنجاح' });
});

app.listen(port, () => {
  console.log(`Server is running on http://localhost:${port}`);
});