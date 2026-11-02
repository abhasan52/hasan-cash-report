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
