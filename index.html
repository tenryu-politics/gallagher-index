<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>ギャラガー指数計算サイト</title>
  <style>
    body { font-family: sans-serif; margin: 20px; }
    input { margin: 5px; width: 80px; }
    table { border-collapse: collapse; margin-top: 20px; }
    th, td { border: 1px solid #ccc; padding: 5px 10px; text-align: right; }
    th { background: #f0f0f0; }
    .note { margin-top: 15px; color: #555; font-size: 0.9em; }
    button.small { font-size: 0.8em; padding: 2px 6px; margin-left: 8px; }
  </style>
</head>
<body>
  <h1>ギャラガー指数 計算</h1>

  <p>全議席: <input type="number" id="totalSeats" value="465"></p>
  <button onclick="addInput()">＋ 政党を追加</button>
  <button onclick="load2024()">🔹 2024衆院選データ</button>
  <button onclick="load2025Sangiin()">🔹 2025参院選データ</button>

  <div id="inputs"></div>
  <button onclick="calculate()">計算</button>

  <h2 id="result"></h2>
  <div id="tableArea"></div>

  <p class="note">
    ※ 党名は任意（未入力でも計算可能）<br>
    ※ 議席を持つ政党はすべて入力してください。<br>
    ※ 議席を持たない政党の得票率は「その他」として計算されます。
  </p>

  <script>
    function addInput(partyName = "", seats = 0, votes = 0) {
      const container = document.getElementById("inputs");
      const index = container.children.length;

      const p = document.createElement("p");
      p.innerHTML = `
        <span class="label">第${index+1}党</span>
        党名（任意）: <input type="text" class="name" value="${partyName}">
        議席数: <input type="number" class="seats" value="${seats}">
        得票率(%): <input type="number" class="votes" value="${votes}">
        <button class="small" onclick="removeInput(this)">削除</button>
      `;
      container.appendChild(p);
    }

    function removeInput(button) {
      button.parentElement.remove();
      renumberParties();
    }

    function renumberParties() {
      const items = document.querySelectorAll("#inputs p");
      items.forEach((p, i) => {
        p.querySelector(".label").textContent = `第${i+1}党`;
      });
    }

    function calculate() {
      const totalSeats = parseInt(document.getElementById("totalSeats").value);
      const inputs = document.querySelectorAll("#inputs p");

      let Sr = [], Vr = [], sumVotes = 0, seatsList = [], nameList = [];

      inputs.forEach(p => {
        const name = p.querySelector(".name").value || `第${nameList.length+1}党`;
        const seats = parseInt(p.querySelector(".seats").value || 0);
        const votes = parseFloat(p.querySelector(".votes").value || 0);
        const seatShare = 100 * seats / totalSeats;
        nameList.push(name);
        Sr.push(seatShare);
        Vr.push(votes);
        seatsList.push(seats);
        sumVotes += votes;
      });

      // その他政党
      Sr.push(0);
      Vr.push(100 - sumVotes);
      seatsList.push(0);
      nameList.push("その他");

      // ギャラガー指数計算
      let z = 0;
      for (let i = 0; i < Sr.length; i++) {
        z += (Vr[i] - Sr[i])**2;
      }
      z = Math.sqrt(z/2);
      document.getElementById("result").textContent = "ギャラガー指数: " + z.toFixed(2);

      // 表作成（%は同じ行に表示）
      let html = `<table>
        <tr><th>党</th><th>議席数</th><th>議席率</th><th>得票率</th></tr>`;
      for (let i = 0; i < Sr.length; i++) {
        html += `<tr>
          <td>${nameList[i]}</td>
          <td>${seatsList[i]}</td>
          <td>${Sr[i].toFixed(2)}%</td>
          <td>${Vr[i].toFixed(2)}%</td>
        </tr>`;
      }
      html += `</table>`;
      document.getElementById("tableArea").innerHTML = html;
    }

    function load2024() {
      const partyNames = [
        "自由民主党",
        "立憲民主党",
        "日本維新の会",
        "国民民主党",
        "公明党",
        "れいわ新選組",
        "日本共産党",
        "参政党",
        "日本保守党",
        "社会民主党"
      ];
      const seats = [191,148,38,28,24,9,8,3,3,1];
      const votes = [26.73,21.20,9.36,11.32,10.93,6.98,6.16,3.43,2.10,1.71];
      const container = document.getElementById("inputs");
      container.innerHTML = "";
      for (let i=0;i<partyNames.length;i++){
        addInput(partyNames[i], seats[i], votes[i]);
      }
      document.getElementById("totalSeats").value = 465;
    }

    function load2025Sangiin() {
      const partyNames = [
        "自由民主党",
        "立憲民主党",
        "国民民主党",
        "参政党",
        "公明党",
        "日本維新の会",
        "日本共産党",
        "れいわ新選組",
        "日本保守党",
        "社会民主党",
        "チームみらい"
      ];
      const seats = [39,22,17,14,8,7,3,3,2,1,1];
      const votes = [21.64,12.50,12.88,12.55,8.80,7.39,4.84,6.56,5.04,2.06,2.56];
      const container = document.getElementById("inputs");
      container.innerHTML = "";
      for (let i=0;i<partyNames.length;i++){
        addInput(partyNames[i], seats[i], votes[i]);
      }
      document.getElementById("totalSeats").value = 125;
    }
  </script>
</body>
</html>
