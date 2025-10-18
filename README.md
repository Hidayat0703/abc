<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Hirys Datapunks | Airdrop Checker</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    body {
      background: linear-gradient(135deg, #003300, #004d00, #001a00);
      font-family: 'JetBrains Mono', monospace;
      color: #d1fae5;
    }
    .neon {
      text-shadow: 0 0 10px #00ff80, 0 0 25px #00ff80;
    }
    .card {
      backdrop-filter: blur(12px);
      background: rgba(0, 30, 0, 0.6);
      border: 1px solid rgba(0, 255, 128, 0.2);
    }
    .input-glow:focus {
      box-shadow: 0 0 10px #00ff80;
      border-color: #00ff80;
      outline: none;
    }
  </style>
</head>
<body class="flex flex-col items-center justify-center min-h-screen">

  <!-- Title -->
  <div class="text-center mb-10">
    <h1 class="text-5xl font-extrabold italic neon">IRYS </h1></h1>
    <p class="mt-3 text-lg italic text-emerald-200">
      Check your eligibility for the <strong>Datapunks Airdrop</strong> 
    </p>
  </div>

  <!-- Airdrop Checker Card -->
  <div class="card p-8 rounded-2xl shadow-xl w-96 text-center transition-all hover:scale-105 hover:shadow-2xl">
    <input
      id="wallet"
      type="text"
      placeholder="Enter your wallet address"
      class="w-full p-3 rounded-lg bg-transparent border border-emerald-400 text-emerald-100 input-glow placeholder-emerald-300 text-sm"
    />

    <button
      onclick="checkAirdrop()"
      class="w-full mt-5 bg-emerald-400 hover:bg-emerald-500 text-black font-bold py-2 px-4 rounded-full shadow-lg transition duration-200"
    >
      Check Airdrop 
    </button>

    <p id="result" class="mt-6 text-emerald-300 text-sm italic"></p>
  </div>

  <!-- Footer -->
  <footer class="mt-12 text-xs text-emerald-400 opacity-60">
    Powered by <strong>Iryna</strong> & <strong>Sprite</strong> | © 2025 IRYS
  </footer>

  <script>
    function checkAirdrop() {
      const wallet = document.getElementById('wallet').value.trim();
      const result = document.getElementById('result');
      if (wallet === '') {
        result.textContent = '⚠️ Please enter your wallet address first.';
        return;
      }

      // Simulate check
      result.textContent = '🔍 Checking eligibility...';
      setTimeout(() => {
        const eligible = Math.random() > 0.5;
        result.textContent = eligible
          ? '✅ Congratulations! You are eligible for the Hirys Datapunks Airdrop.'
          : '❌ Sorry, this wallet is not eligible.';
      }, 1200);
    }
  </script>

</body>
</html>
