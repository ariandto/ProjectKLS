function onEdit(e){
  oE1(e);
  oE2(e);
  }
function oE1(e){
  var ss = SpreadsheetApp.getActive().getActiveSheet();
  //Lokasi spesifik cell 1 baris
  var selection = ss.getActiveCell().getA1Notation().split("");
  var row = ss.getActiveCell().getRow();
  //Checkbox approval by admin di kolom J
  var checkBoxValue = ss.getActiveCell().getValue().toString();
//Copy paste approvak by admin jika di checklist di kolom J
  if(selection[0] != "J") {
    return;}
  switch(checkBoxValue){
    case checkBoxValue = "true":
      ss.getRange("B6:D250").copyTo(ss.getRange("B6"), {contentsOnly:true});
      ss.getRange("L6:O250").copyTo(ss.getRange("L6"), {contentsOnly:true});
      ss.getRange("I6:I250").copyTo(ss.getRange("I6"), {contentsOnly:true});
      ss.getRange("P1").copyTo(ss.getRange("P1"), {contentsOnly:true});      
      break;
  }
}
//TIMESTAMP IN OUT DRIVER
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
function onEdit(e){
  oE1(e);
  oE2(e);
  }
function oE1(e){
  var ss = SpreadsheetApp.getActive().getActiveSheet();
  //Lokasi spesifik cell 1 baris
  var selection = ss.getActiveCell().getA1Notation().split("");
  var row = ss.getActiveCell().getRow();
  //Checkbox approval by admin di kolom J
  var checkBoxValue = ss.getActiveCell().getValue().toString();
//Copy paste approvak by admin jika di checklist di kolom J
  if(selection[0] != "J") {
    return;}
  switch(checkBoxValue){
    case checkBoxValue = "true":
      ss.getRange("B6:D250").copyTo(ss.getRange("B6"), {contentsOnly:true});
      ss.getRange("L6:O250").copyTo(ss.getRange("L6"), {contentsOnly:true});
      ss.getRange("I6:I250").copyTo(ss.getRange("I6"), {contentsOnly:true});
      ss.getRange("P1").copyTo(ss.getRange("P1"), {contentsOnly:true});      
      break;
  }
}
//TIMESTAMP IN OUT DRIVER
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
