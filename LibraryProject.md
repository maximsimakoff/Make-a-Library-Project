//US PRESIDENT DATA SET
//Different Search's
//1 - Home state check
//2 - Portait
//3 - Political Party
//4 - Took office
//5 - Left office
//6 - Random President
//7 - check presidency

/*----------------------------------------------------------------------------------*/

//1
//This function finds out the president and the user guess's the state.
function president_homestate_check(guess) {
var allPresidenthome = getColumn("US Presidents", "Home state");
var count = 0;
for (var i = 0; i<allPresidenthome.length; i++) {
if(guess == allPresidenthome[i]){
count = count++;  
}
}
return count;
}

//2
//This function attachs a  random president to the corresponding image
function portraitImage(id) {
var picture;
readRecords("US Presidents", {}, function(pres_records) {
if (pres_records.length>0) {
picture = ("id: " + pres_records[id].id) + " President: " +pres_records[id].President+ " Picture url: " + pres_records[id].Portrait;
}
});
return picture;
}

//3
//This function finds out what the specific president's party is 
function portraitImage(id) {
var party;
readRecords("US Presidents", {}, function(pres_records) {
if (pres_records.length>0) {
party = "id: " + pres_records[id].id + " President: " +pres_records[id].President+ " Political Party: " + pres_records[id].Party;
}
});
return party;
}

//4
//This function finds out when the specific president has took the office
function portraitImage(id) {
var took_office;
readRecords("US Presidents", {}, function(pres_records) {
if (pres_records.length>0) {
took_office = "id: " + pres_records[id].id + " President: " +pres_records[id].President+ " took office: " + pres_records[id].Tookoffice;
}
});
return took_office;
}

//5
//This function finds out when the specific president has left the office
function portraitImage(id) {
var left_office;
readRecords("US Presidents", {}, function(pres_records) {
if (pres_records.length>0) {
left_office = "id: " + pres_records[id].id + " President: " +pres_records[id].President+ " Left office: " + pres_records[id].Leftoffice;
}
});
return left_office;
}

//6
//This function pulls a random president
function randomPresident() {
var presidentName = getColumn("US Presidents", "President");
var index = randomNumber(0, presidentName.length-1);  
var index_name = presidentName[index];
return index_name;
}

//7
//Check presidency
function check_presidency(guess, index) {
var correct = false;
var presidency = getColumn("US Presidents", "Presidency");
if (guess == presidency[index]) {
correct=true;  
}
return correct;
}
/*----------------------------------------------------------------------------------*/
