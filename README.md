MultipleChoiceController-iOS
============================

This class lets you quickly implement a multiple-selection list screen in your iOS application. To use:

```swift
...

let vc = MultipleChoiceController(style: UITableViewStyle.Grouped)
vc.choices = ["Apples", "Oranges", "Bananas"] //Provide an array of choices. These must be NSObjects.

vc.allowMultipleSelections = true
vc.maximumAllowedSelections = 2 // Optional, limits selection.

vc.header = "Choose some fruits" // A header that appears before the list.
vc.footer = "Make sure to choose some delicious ones!" //A footer that appears after the list.
vc.delegate = self //Implement the MultipleChoiceControllerDelegate protocol to handle selections.

self.navigationController?.pushViewController(vc, animated: true)

...

/* Delegate method when selection is finished */

func multipleChoiceController(controller: MultipleChoiceController, didSelectItems items: [NSObject]) {
  //Do something with the "items" the user selected.
  navigationController?.popViewControllerAnimated(true)
}

```
