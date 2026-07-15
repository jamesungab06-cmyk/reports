<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Reports and Analytics</title>

<link rel="stylesheet"
href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.7.1/css/all.min.css">

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Segoe UI',sans-serif;
}

body{
    display:flex;
    background:#f3f4f9;
}

/* SIDEBAR */

.sidebar{
    width:250px;
    height:100vh;
    background:linear-gradient(180deg,#001B4D,#012B70);
    position:fixed;
    left:0;
    top:0;
    overflow-y:auto;
    padding-top:20px;
}

.menu{
    list-style:none;
}

.menu li{
    margin:12px 15px;
}

.menu li a{
    display:flex;
    align-items:center;
    gap:15px;
    color:white;
    text-decoration:none;
    padding:18px 20px;
    border-radius:20px;
    font-size:20px;
    transition:0.3s;
}

.menu li a:hover{
    background:#2E66F5;
}

.menu .active a{
    background:#2E66F5;
    box-shadow:0 5px 20px rgba(46,102,245,.5);
}

/* MAIN */

.main{
    margin-left:270px;
    width:calc(100% - 270px);
    padding:30px;
}

.title{
    font-size:55px;
    color:#103C77;
    font-weight:bold;
    margin-bottom:30px;
}

/* FILTERS */

.filters{
    display:flex;
    gap:15px;
    align-items:flex-end;
    margin-bottom:30px;
    flex-wrap:wrap;
}

.filter-group{
    display:flex;
    flex-direction:column;
}

.filter-group label{
    margin-bottom:8px;
    color:#555;
}

input,select{
    width:220px;
    padding:12px;
    border:1px solid #ccc;
    border-radius:6px;
}

button{
    border:none;
    color:white;
    padding:12px 20px;
    border-radius:6px;
    font-weight:bold;
    cursor:pointer;
}

.generate{
    background:#28A745;
}

.download{
    background:#0D6EFD;
}

.print{
    background:#6C757D;
}

/* CONTENT */

.content{
    display:flex;
    gap:20px;
}

.report-box{
    flex:1;
    background:white;
    border-radius:15px;
    padding:25px;
    box-shadow:0 2px 10px rgba(0,0,0,.05);
}

.summary-box{
    width:300px;
    background:white;
    border-radius:15px;
    padding:25px;
    box-shadow:0 2px 10px rgba(0,0,0,.05);
}

.section-title{
    font-size:35px;
    font-weight:bold;
    margin-bottom:25px;
}

/* TABLE */

table{
    width:100%;
    border-collapse:collapse;
}

th{
    background:#072B67;
    color:white;
    padding:15px;
}

td{
    padding:15px;
    border-bottom:1px solid #ddd;
    text-align:center;
}

.pass{
    color:green;
    font-weight:bold;
}

.fail{
    color:red;
    font-weight:bold;
}

/* SUMMARY */

.summary-item{
    margin-bottom:35px;
}

.summary-item h4{
    color:#12396E;
    font-size:28px;
    margin-bottom:10px;
}

.summary-item p{
    color:#555;
    font-size:22px;
}

</style>
</head>

<body>

<div class="sidebar">

<ul class="menu">

<li><a href="#"><i class="fa-solid fa-table-columns"></i> Dashboard</a></li>

<li><a href="#"><i class="fa-solid fa-user"></i> User Management</a></li>

<li><a href="#"><i class="fa-solid fa-file-lines"></i> Review Management</a></li>

<li><a href="#"><i class="fa-solid fa-chart-line"></i> User Engagement</a></li>

<li><a href="#"><i class="fa-solid fa-database"></i> Test Banking</a></li>

<li><a href="#"><i class="fa-solid fa-pencil"></i> Test Construction</a></li>

<li><a href="#"><i class="fa-solid fa-gear"></i> Test Administration</a></li>

<li class="active">
<a href="#"><i class="fa-solid fa-chart-column"></i> Reports</a>
</li>

<li><a href="#"><i class="fa-solid fa-right-from-bracket"></i> Logout</a></li>

</ul>

</div>

<div class="main">

<div class="title">Reports and Analytics</div>

<div class="filters">

<div class="filter-group">
<label>Search Student</label>
<input type="text" placeholder="Search by Name">
</div>

<div class="filter-group">
<label>Category</label>
<select>
<option>Practice Quiz 1</option>
<option>Practice Quiz 2</option>
<option>Practice Quiz 3</option>
<option>Practice Quiz 4</option>
<option>Exam</option>
</select>
</div>

<div class="filter-group">
<label>View</label>
<select>
<option>Top 10 Students</option>
<option>Failed Students</option>
</select>
</div>

<button class="generate">Generate Report</button>
<button class="download">Download</button>
<button class="print" onclick="window.print()">Print</button>

</div>

<div class="content">

<div class="report-box">

<div class="section-title">
Practice Quiz 1 - Top 10 Students
</div>

<table>

<tr>
<th>Rank</th>
<th>Student Name</th>
<th>Score</th>
<th>Status</th>
</tr>

<tr><td>1</td><td>Maria Santos</td><td>98%</td><td class="pass">Passed</td></tr>
<tr><td>2</td><td>Juan Dela Cruz</td><td>97%</td><td class="pass">Passed</td></tr>
<tr><td>3</td><td>Ana Reyes</td><td>96%</td><td class="pass">Passed</td></tr>
<tr><td>4</td><td>Mark Lim</td><td>95%</td><td class="pass">Passed</td></tr>
<tr><td>5</td><td>Carla Garcia</td><td>94%</td><td class="pass">Passed</td></tr>
<tr><td>6</td><td>Paul David</td><td>93%</td><td class="pass">Passed</td></tr>
<tr><td>7</td><td>Joyce Lim</td><td>92%</td><td class="pass">Passed</td></tr>
<tr><td>8</td><td>Ken Cruz</td><td>91%</td><td class="pass">Passed</td></tr>
<tr><td>9</td><td>Claire Tan</td><td>90%</td><td class="pass">Passed</td></tr>
<tr><td>10</td><td>Ben Cruz</td><td>89%</td><td class="pass">Passed</td></tr>

</table>

</div>

<div class="summary-box">

<div class="summary-item">
<h4>Total Students</h4>
<p>125</p>
</div>

<div class="summary-item">
<h4>Passed Students</h4>
<p>98 (78.4%)</p>
</div>

<div class="summary-item">
<h4>Failed Students</h4>
<p>27 (21.6%)</p>
</div>

<div class="summary-item">
<h4>Highest Score</h4>
<p>98%</p>
</div>

<div class="summary-item">
<h4>Lowest Score</h4>
<p>52%</p>
</div>

<div class="summary-item">
<h4>Current Category</h4>
<p>Practice Quiz 1</p>
</div>

</div>

</div>

</div>

</body>
</html>
