// Initialize Firebase
var config = {
    apiKey: "AIzaSyCtBPR7BDFclI-fNS7D2d8HW4YLnPcwWq8",
    authDomain: "fireformdata-ff691.firebaseapp.com",
    databaseURL: "https://fireformdata-ff691.firebaseio.com",
    projectId: "fireformdata-ff691",
    storageBucket: "fireformdata-ff691.appspot.com",
    messagingSenderId: "155146186514"
  };
firebase.initializeApp(config);
var messagesRef = firebase.database().ref('fireformdata');

// listen to form submit
document.getElementById('fireform').addEventListener('submit', submitForm);

//submit form
function submitForm(e) {
    e.preventDefault();
    //get values
    var email = getInputVal('email_input');
    var email1 = getInputVal('email_input');
    var data_structure = [email, email1, email]
    //save messages
    saveMessage(data_structure);
    // show alert error
    document.querySelector('#sub').style.display = 'block';
    //hide alert after 3 seconds
    setTimeout(function() {
        document.querySelector('#sub').style.display = 'none';
    }, 3000);
}

function getInputVal(id) {
    return document.getElementById(id).value;
}

//save message to firebase
function saveMessage(data_structure) {
    var newMessageRef = messagesRef.push();
    newMessageRef.set({
        first_name: data_structure[0],
        last_name: data_structure[1],
        email: data_structure[2]
    });
}
