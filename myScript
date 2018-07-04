// Student Manager List.
var arrStudent = [
     //  create array objects of sudent list.
     {
          "studentCode" :1,
          "studentName" :"Sok Vannak",
          "className"   : "C1711L"
     },
     {
          "studentCode" :2,
          "studentName" :"Sok Dara",
          "className"   : "C1709L"
     },
     {
          "studentCode" :3,
          "studentName" :"Sok Chan Tha",
          "className"   : "C1705L"
     },
     {
          "studentCode" :4,
          "studentName" :"Sok Vy",
          "className"   : "C1704L"
     },
];

window.onload = loadData;
//  loading data after array lists student object created.

function loadData(){
// create a function loadData (name) to make a table student list objects.
     var studentList = document.getElementById("studentList");
     //  studentList is a table id had created, we have some element tags
     //  table, tr, th, td and another element tags..
     for (var i = 0; i < arrStudent.length; i++){
          var trNode = document.createElement("tr");
          studentList.appendChild(trNode);

     /*   1. create a td_1 variable to create td element tag.
          2. get td_1 variable to appendChild trNote had appendChild os StudentList variable.
          3. create a td_1 variable to create text node and to get arrStudent[i].studentCode
             had created in function of array objects of student list.
          4. get td_1 variable to appendChild of studentCode variable by arrStudent[i].studentCode.
     */
          var td_1 = document.createElement("td");
          trNode.appendChild(td_1);
          var studentCodeNode = document.createTextNode(arrStudent[i].studentCode);
          td_1.appendChild(studentCodeNode);

          var td_2 = document.createElement("td");
          trNode.appendChild(td_2);
          var studentNameNode = document.createTextNode(arrStudent[i].studentName);
          td_2.appendChild(studentNameNode);

          var td_3 = document.createElement("td");
          trNode.appendChild(td_3);
          var classNameNode = document.createTextNode(arrStudent[i].className);
          td_3.appendChild(classNameNode);

          var td_4 = document.createElement("td");
          trNode.appendChild(td_4);
          //  set seleteBtn variable to get button type.
          var btnselete = document.createElement("button");
          btnselete.type = "button";
          //  set attribute of seleteBtn variable to get cnclick function.
          btnselete.setAttribute("onclick","Selete(" + i + ")");
          td_4.appendChild(btnselete);

          var btnselelteString = document.createTextNode("Selete");
          btnselete.appendChild(btnselelteString);
     }
}

function clearTable(){
     //  set clearTable function to clear studentList in the table.
     var StudentList = document.getElementById("studentList");

     // this condition to remove the last child of StudentList variable.
     while(StudentList.children.length >1){
          StudentList.removeChild(StudentList.lastChild);
     }
}

function AddNew(){
     // create a function to add new student on sign up form.
     var idStudent = document.getElementById("txtstudentCode").value;
     var StudentName = document.getElementById("txtstudentName").value;
     var idClass = document.getElementById("classCode").value;

     // condition to excuted when empty sign up type box.
     if(idStudent === "" || StudentName === ""){
          return;
     }

     //  set arrStudent of function to push student objects list.
     arrStudent.push({
          "studentCode" :idStudent,
          "studentName" :StudentName,
          "className"   :idClass  
     });

     //  call all functions clearTable and loadData.
     clearTable();
     loadData();
}

function Delete(){
     var idStudent = document.getElementById("txtstudentCode").value;

     if(txtstudentCode === ""){
          return;
     }

     txtstudentCode = parseInt(txtstudentCode);

           // this condition to compare arrStudent[i].studentCode with idStudent variable to remove objects.
     for(var i = 0; i < arrStudent.length; i++){
          if(arrStudent[i].studentCode == idStudent){
               break;
          }
     }
          //  this condition to remove student object in arrStudentList.
     if(i < arrStudent.length){
          arrStudent.splice(i,1);
     }

     clearTable();
     loadData();
}

function Update(){
     // create a function to uypdate student on sign up form.
     var idStudent = document.getElementById("txtstudentCode").value;
     var StudentName = document.getElementById("txtstudentName").value;
     var idClass = document.getElementById("classCode").value;

     if(idStudent === "" || StudentName === ""){
          return;
     }

     for(var i = 0; i < arrStudent.length; i++){
          if(arrStudent[i].studentCode == idStudent){
               break;
          }
     }
          // this condition to compare arrStudent[i].'objects' with all variables to updating objects.
     if(i < arrStudent.length){
          arrStudent[i].studentCode = idStudent;
          arrStudent[i].studentName = StudentName;
          arrStudent[i].className = idClass;
     }

     clearTable();
     loadData();
}

function Selete(i){
     // create a function to get objects in arrStudent list to show on sign up of form element. 
     document.getElementById("txtstudentCode").value = arrStudent[i].studentCode;
     document.getElementById("txtstudentName").value = arrStudent[i].studentName;
     //  set variable to compare with arrStudent[i].className in seletion element tag.
     var idClassNode = document.getElementById("classCode");
     idClassNode.value = arrStudent[i].className;
}


