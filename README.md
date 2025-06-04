!DOCTYPE html>
<html lang="th">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>GOLfMINIX2 PANEL FREE v1.0</title>
  <style>
    body {
      background: black;
      font-family: sans-serif;
      color: white;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .menu {
      background: #111;
      border: 2px solid yellow;
      box-shadow: 0 0 20px yellow;
      border-radius: 10px;
      padding: 20px;
      width: 300px;
    }
    h2 {
      color: yellow;
      text-align: center;
    }
    label, select, input[type=\"checkbox\"] {
      margin-top: 10px;
      display: block;
    }
    select, input[type=range] {
      width: 100%;
      padding: 5px;
      border-radius: 5px;
      background: #222;
      color: white;
      border: 1px solid yellow;
    }
    input[type=checkbox] {
      display: inline-block;
      margin-right: 5px;
    }
  </style>
</head>
<body><script>
  // เมื่อเลือกโหมดยิงหัว
  document.querySelectorAll('select')[0].addEventListener('change', function () {
    alert('คุณเลือกโหมดยิงหัว: ' + this.value);
  });

  // เมื่อเช็ค/ยกเลิก checkbox “เปิดดูดหัว”
  document.querySelector('input[type=checkbox]').addEventListener('change', function () {
    if (this.checked) {
      alert('ระบบดูดหัว: เปิดใช้งาน');
    } else {
      alert('ระบบดูดหัว: ปิดแล้ว');
    }
  });

  // แสดงค่าจาก slider
  const slider = document.querySelector('input[type=range]');
  slider.addEventListener('input', function () {
    this.title = 'ความไว: ' + this.value; // แสดงค่าเมื่อ hover
  });
</script>

  <div class="menu">
    <h2>GOLfMINIX2 PANEL FREE v1.0</h2>
    <label><input type="checkbox" checked /> เปิดดูดหัว</label>

    <label>เลือกโหมดยิงหัว</label>
    <select>
      <option>HIGH = สูง</option>
      <option>MEDIUM = กลาง</option>
      <option>LOW = ต่ำ</option>
    </select>

    <label>เลือกโหมดแมพที่เล่น</label>
    <select>
      <option>1-1</option>

    </select>

    <label><input type="checkbox" /> จอไว จอลื่นขึ้น</label>
    <label><input type="checkbox" /> แก้เกมกระตุก</label>
    <label><input type="checkbox" /> เพิ่มความไวของปุ่มยิง</label>
    <label><input type="checkbox" /> บายพาสดูดหัส</label>
    <label><input type="checkbox" /> กันโดนแบน - กันดำ - กันรายงาน</label>

    <div class="slider-container">
      <label>ปรับความไวการลากหัว</label>
      <input type="range" min="0" max="100" value="50" />
    </div>
  </div>
<script>
  // โหมดดูดหัว
  const headshotToggle = document.querySelector('input[type="checkbox"]');
  headshotToggle.addEventListener('change', function () {
    alert(this.checked ? "เปิดระบบดูดหัว" : "ปิดระบบดูดหัว");
  });

  // เลือกโหมดยิงหัว
  const shootMode = document.querySelectorAll('select')[0];
  shootMode.addEventListener('change', function () {
    alert("โหมดที่เลือก: " + this.value);
  });

  // ความไวจาก slider
  const slider = document.querySelector('input[type="range"]');
  slider.addEventListener('input', function () {
    this.title = "ความไว: " + this.value;
  });
</script>
</html>
