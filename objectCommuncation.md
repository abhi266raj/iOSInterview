* When should you use KVO and when delegate. 
* Which is better KVO, delegate or NotificationCentre
* In a hospital there is a notice board. The notice will show the next patient to meet doctor. How will you code this. Should patient know about existence of notice-board? Should noticeboard know about existence of patinet object. Will there will be same sitaution when there can be one notice board vs multiple noticeboard.
 
```
class NoticeBoard {
static var shared = NoticeBoard()
var text:String?
}

class Patient {
var name:String

func enterHospital() {
//Implementit
}

func meetDoctor() {
//Implemented
}
```

* There are two classes Engineer and labourer. Labourer will make the machine but need to ask question from engineer like what should be size of machine, what should be number of machine to make etc. Implement that.

* In a bus stand bus comes and conductor annouces which bus no and the destination where will it go. The passenger check the destination and board the bus. Implement that.

