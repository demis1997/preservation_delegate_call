# preservation_delegate_call
 using delegate call for set time vulnerability

the key to this is to have the exact same layout so that when you call setfirsttime then you can overwrite it with the attacking contract and make the delegation call the second time making us the owner. The part of the code to look at is this:

constructor(address _timeZone1LibraryAddress, address _timeZone2LibraryAddress) public {
    timeZone1Library = _timeZone1LibraryAddress; 
    timeZone2Library = _timeZone2LibraryAddress; 
    owner = msg.sender;
  }
 
<img width="1929" alt="preservation" src="https://user-images.githubusercontent.com/63403890/186509129-02d92dcf-64af-4b10-baf5-e462b7420a26.png">
