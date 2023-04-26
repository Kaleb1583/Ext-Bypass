# Ext-Bypass
disable any google extension or management forced extensions 


# ---------------- For My School ---------------------
var currentURL = document.location.href;
if(currentURL == "chrome-extension://gndmhdcefbhlchkhipcnnbkcmicncehk/manifest.json") {
    var examples = ["fgkpjlnpnfhidpnjmfbccefcifcfalhi", "gcjpefhffmcgplgklffgbebganmhffje"];
    var names = ["Cipafilter Direct Authenticator", "NetSupport School Student"];
    
    var id = prompt("1: Cipafilter, 2: NetSupport"); // EXTENSION ID
    
    if(id == 1) {
        id = examples[0];
    }
    
    if(id == 2) {
        id = examples[1];
    }
    
    var able = prompt("0: Disable & 1: Enable"); // ENABLE / DISABLE

    if(able == 0) {
        able = "disable";
        if(id.length == 32) {
            chrome.management.setEnabled(String(id), false)
        }
    }

    if(able == 1) {
        able = "enable";
        if(id.length == 32) {
            chrome.management.setEnabled(String(id), true)
        }
    }
} else {
    alert("you need to go to a chrome extension's manifest.json file!")
    alert("Try: chrome-extension://gndmhdcefbhlchkhipcnnbkcmicncehk/manifest.json")
}
#------------------------------------------------------------
