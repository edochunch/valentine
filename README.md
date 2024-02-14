<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Valentine's Day Page</title>
  <style>
  .flex {
    display: flex;
    }
    .flex-col {
      flex-direction: column;
    }
    .items-center {
      align-items: center;
    }
    .justify-center {
      justify-content: center;
    }
    .h-screen {
      height: 100vh;
    }
    .-mt-16 {
      margin-top: -16px;
    }
    .text-4xl {
      font-size: 2rem;
    }
    .font-bold {
      font-weight: bold;
    }
    .my-4 {
      margin-top: 1rem;
      margin-bottom: 1rem;
    }
    .py-2 {
      padding-top: 0.5rem;
      padding-bottom: 0.5rem;
    }
    .px-4 {
      padding-left: 1rem;
      padding-right: 1rem;
    }
    .rounded {
      border-radius: 0.25rem;
    }
    .bg-green-500 {
      background-color: #34d399;
    }
    .bg-green-700 {
      background-color: #10b981;
    }
    .hover\:bg-green-700:hover {
      background-color: #10b981;
    }
    .text-white {
      color: #fff;
    }
    .bg-red-500 {
      background-color: #ef4444;
    }
    .bg-red-700 {
      background-color: #dc2626;
    }
    .hover\:bg-red-700:hover {
      background-color: #dc2626;
    }
  </style>
</head>
<body>
  <div class="flex flex-col items-center justify-center h-screen -mt-16">
    <img class="h-[200px]" src="https://gifdb.com/images/high/cute-love-bear-roses-ou7zho5oosxnpo6k.gif" />
    <h1 class="text-4xl my-4">WILL U GO ON A DATE WITH ME TODAY ISH <3?</h1>
    <div>
      <button class="bg-green-500 hover:bg-green-700 text-white font-bold py-2 px-4 rounded" style="font-size: 16px;" onclick="setYesPressed(true)">Yes</button>
      <button class="bg-red-500 hover:bg-red-700 text-white font-bold py-2 px-4 rounded" onclick="handleNoClick()">No</button>
    </div>
  </div>

  <script>
    let noCount = 0;
    let yesPressed = false;

    function handleNoClick() {
      noCount++;
      document.querySelector('button:nth-child(2)').textContent = getNoButtonText();
    }

    function getNoButtonText() {
      const phrases = [
        "No",
        "Are you sure manan?",
        "Really! Are u really sure ish ;(",
        "Think again!",
        "Last chance!",
        "Surely not?",
        "You might regret this!",
        "Give it another thought!",
        "Are you absolutely certain?",
        "This could be a mistake!",
        "Have a heart!",
        "Don't be so cold!",
        "Change of heart?",
        "Wouldn't you reconsider?",
        "Is that your final answer Ish?",
        "You're breaking my heart. I'm sad. Now come and meet me pookie."
      ];

      return phrases[Math.min(noCount, phrases.length - 1)];
    }

    function setYesPressed(value) {
      yesPressed = value;
      if (yesPressed) {
        document.querySelector('.flex div').innerHTML = '<img src="https://media.tenor.com/gUiu1zyxfzYAAAAi/bear-kiss-bear-kisses.gif" /><div class="text-4xl font-bold my-4">Ok yay!!!</div>';
      }
    }
  </script>
</body>
</html>
