- 👋 Hi, I’m @Sarathisarathi2
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
<!DOCTYPE html>
<html>
  <head>
    <style>
      body {
        display: table;
        font-family: "Helvetica Neue", sans-serif;
        margin: 8px auto;
      }
      input {
        border: none;
        border-bottom: 1px dashed #888;
        text-align: right;
        width: 108px;        
      }
      div {
        color: #aaa;
        margin-bottom: 8px;
      }
      .indian {
        color: black;
      }
      .unit {
        display: inline-block;
        margin-left: 8px;
        width: 76px;
      }
      .zero {
        font-size: 14px;
        margin-left: 8px;
      }
    </style>
  </head>
  <body>
    <div>
      <input type="number" divisor="1"></input>
    </div>
    <div>
      <input type="number" divisor="1e3"></input><span class="unit">thousand</span><span class="zero">3 zeros</span>
    </div>
    <div class="indian">
      <input type="number" divisor="1e5"></input><span class="unit">lakh</span><span class="zero">5 zeros</span>
    </div>
    <div>
      <input type="number" divisor="1e6"></input><span class="unit">million</span><span class="zero">6 zeros</span>
    </div>
    <div class="indian">
      <input type="number" divisor="1e7"></input><span class="unit">crore</span><span class="zero">7 zeros</span>
    </div>
    <div>
      <input type="number" divisor="1e9"></input><span class="unit">billion</span><span class="zero">9 zeros</span>
    </div>
    <div>
      <input type="number" divisor="1e12"></input><span class="unit">trillion</span><span class="zero">12 zeros</span>
    </div>
    <div class="indian">
      <input type="number" divisor="1e12"></input><span class="unit">lakh crore</span><span class="zero">12 zeros</span>
    </div>

    <script>
      const inputs = document.querySelectorAll("input");
      
      inputs.forEach((i0, i) => {
        i0.addEventListener("keyup", ({ target }) => {
          const v = +target.value * +target.getAttribute("divisor");
          inputs.forEach(i1 => {
            i1.value = v / +i1.getAttribute("divisor");
          });
        });

        if (i === 0) i0.focus();
      });
    </script>
  </body>
</html>

<!---
Sarathisarathi2/Sarathisarathi2 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
