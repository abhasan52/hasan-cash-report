<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>School Attendance System</title>
<link rel="stylesheet" href="style.css">
</head>
<body>
<header>
  <h1>🏫 School Attendance System</h1>
  <nav>
    <button data-tab="checkin" class="active">Check In / Out</button>
    <button data-tab="students">Students</button>
    <button data-tab="records">Attendance Records</button>
  </nav>
</header>

<main>
<section id="checkin" class="tab active">
  <div class="card">
    <h2>Student Check-In / Check-Out</h2>
    <form id="attendanceForm">
      <label>Student ID</label>
      <input id="studentId" placeholder="Enter student ID" required>
      <label>Action</label>
      <select id="action">
        <option value="Check In">Check In</option>
        <option value="Check Out">Check Out</option>
      </select>
      <button type="submit">Save Attendance</button>
    </form>
    <p id="attendanceMessage"></p>
  </div>
</section>

<section id="students" class="tab">
  <div class="card">
    <h2>Add Student</h2>
    <form id="studentForm">
      <label>Student ID</label>
      <input id="newId" required>
      <label>Full Name</label>
      <input id="newName" required>
      <label>Class</label>
      <input id="newClass" required>
      <button type="submit">Add Student</button>
    </form>
  </div>
  <div class="card">
    <h2>Student List</h2>
    <table id="studentTable">
      <thead><tr><th>ID</th><th>Name</th><th>Class</th><th>Status</th></tr></thead>
      <tbody></tbody>
    </table>
  </div>
</section>

<section id="records" class="tab">
  <div class="card">
    <h2>Attendance Records</h2>
    <button id="clearRecords" class="danger">Clear All Records</button>
    <table id="recordTable">
      <thead><tr><th>Date</th><th>Student ID</th><th>Name</th><th>Action</th><th>Time</th></tr></thead>
      <tbody></tbody>
    </table>
  </div>
</section>
</main>

<script src="app.js"></script>
</body>
</html>

*{box-sizing:border-box;font-family:Arial,sans-serif}
body{margin:0;background:#f2f5f9;color:#1f2937}
header{background:#1d4ed8;color:#fff;padding:18px 24px}
header h1{margin:0 0 12px;font-size:22px}
nav button{background:rgba(255,255,255,.15);color:#fff;border:0;padding:9px 16px;margin-right:8px;border-radius:8px;cursor:pointer}
nav button.active{background:#fff;color:#1d4ed8;font-weight:bold}
main{padding:24px;max-width:1000px;margin:auto}
.tab{display:none}
.tab.active{display:block}
.card{background:#fff;border-radius:12px;padding:20px;margin-bottom:20px;box-shadow:0 2px 8px rgba(0,0,0,.08)}
label{display:block;margin:10px 0 5px;font-weight:bold}
input,select{width:100%;padding:10px;border:1px solid #cbd5e1;border-radius:8px;margin-bottom:10px}
button{background:#1d4ed8;color:#fff;border:0;padding:11px 18px;border-radius:8px;cursor:pointer}
button:hover{opacity:.9}
.danger{background:#dc2626}
table{width:100%;border-collapse:collapse;margin-top:12px}
th,td{border-bottom:1px solid #e5e7eb;padding:10px;text-align:left}
th{background:#eff6ff}
#attendanceMessage{font-weight:bold}

