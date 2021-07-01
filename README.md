# Time Picker Plus  
  
## Features  
* 2 new modes dialOnly and inputOnly - now, you can hide change mode (IconButton)  
  
I've changed type of initialEntryMode from TimePickerEntryMode to TimePickerPlusEntryMode, which  
now has more modes.  
  
*Old:*  
**TimePickerEntryMode:**  
* **dial** - Tapping/dragging on a clock dial  
* **input** - Text input  
  
*New:*  
**TimePickerPlusEntryMode:**  
* **dial** - default use dial mode from TimePickerEntryMode  
* **input** - default use input mode from TimePickerEntryMode  
* **dialOnly** - use only dial mode (blocks opportunity to change mode)  
* **inputOnly** - use only input mode (blocks opportunity to change mode)  
  
## Usage  
Just use s*howTimePickerPlus()* instead of *showTimePicker()* - it's really that simple!  
  
```
import 'package:time_picker_plus/time_picker_plus.dart'

Future<TimeOfDay> show(BuildContext context) async {
    final TimeOfDay pickedDate = await showTimePickerPlus(
        context: context,
        initialTime: TimeOfDay.now(),
        initialEntryMode: TimePickerPlusEntryMode.dialOnly,
    );
    return pickedDate;
}
```
