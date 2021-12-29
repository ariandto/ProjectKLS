# ProjectKLS
'''javascript

function onEdit(e){
  oE1(e);
  oE2(e);
  }

function oE1(e){
  var ss = SpreadsheetApp.getActive().getActiveSheet();
  //Gets the Location where user cliks on the sheet
  var selection = ss.getActiveCell().getA1Notation().split("");
  var row = ss.getActiveCell().getRow();
  //CHECKBOX
  var checkBoxValue = ss.getActiveCell().getValue().toString();

  //RUN IN
  if(selection[0] != "J") {
    return;}
  switch(checkBoxValue){
    case checkBoxValue = "true":
      ss.getRange("B6:C250").copyTo(ss.getRange("B6"), {contentsOnly:true});
      ss.getRange("L6:N250").copyTo(ss.getRange("L6"), {contentsOnly:true});
      ss.getRange("O1").copyTo(ss.getRange("O1"), {contentsOnly:true});

      
      break;
  }
}
//TIMESTAMP
function oE2(e){
  if(e.value != "TRUE" ) return;
  var date = new Date();
  var hour = date.getHours() < 10 ? "0" + date.getHours() : date.getHours();
  var min = date.getMinutes() < 10 ? "0" + date.getMinutes() : date.getMinutes();
  var sheet = SpreadsheetApp.getActiveSheet();
  var value = e.source.getActiveSheet().getRange(e.range.rowStart,e.range.columnStart+0).setValue(hour + ":" + min);
  var tampilWaktu = "Jam: " + jam + ":" + menit
  Logger.log([value.getHours(), value.getMinutes()]); 
}
```