# iOS Troubleshooting

## Keyboard does not appear on Simulator when you tap inside a text field

Root cause: One potential reason is that the hardware keyboard is enabled. You can confirm this by checking if NSNotification for keyboardWillShow and keyboardWillHide are mixed up \(i.e when you tap inside a text field, the notification keyboardWillHide is sent instead of keyboardWillShow\)

Solution: Press Cmd+K \(Toggle keyboard\) on the simulator window.

## Unnecessary vertical blank space at the top of UITableView <a id="unnecessary-vertical-blank-space-at-the-top-of-uitableview"></a>

[https://stackoverflow.com/questions/18880341/why-is-there-extra-padding-at-the-top-of-my-uitableview-with-style-uitableviewst?utm\_medium=organic&utm\_source=google\_rich\_qa&utm\_campaign=google\_rich\_qa](https://stackoverflow.com/questions/18880341/why-is-there-extra-padding-at-the-top-of-my-uitableview-with-style-uitableviewst?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa)

## A table view looks crooked on iOS 10 only

* Check if the tableView's estimatedRowHeight is set. On iOS 10, it has to be set explicitly sometimes.

## LaunchDarkly FeatureFlag Has Default Value, Not Actual Value

* Make sure that you are pointing to the same LD environment as the QBSE server environment
* Make sure that the Targeting is ON
* Make sure that the user is not excluded by any rule
* If you added a specific user-based rule, make sure that the userid is available in LD



