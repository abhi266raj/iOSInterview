* When should u use KVO and when delegate. 
* Which is better KVO, delegate or NotificationCentre
* In a hospital there is a notice board. The notice will show the next patient to meet doctor. How will you code this. Should patient know about existence of notice-board? Should noticeboard know about existence of patinet object.
 
```
class NoticeBoard {
static var shared = NoticeBoard()
var nextPatientName:String?
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