UIBarButtonItem-blocks
==================

***Category on UIBarButtonItem that implements block support***

This category adds block support for `UIBarButtonItem`.
All default methods of the `UIBarButtonItem` init family are implemented.
You can also create an instance with custom view and use `-setActionHandler:` later in code.

##Example usage
``` objective-c
- (void)viewDidLoad {
  [super viewDidLoad];
  
  [[self navigationItem] setRightBarButtonItem:[[UIBarButtonItem alloc] initWithBarButtonSystemItem:UIBarButtonSystemItemAction actionHandler:^{
  	UIActivityViewController *shareController = [[UIActivityViewController alloc] initWithActivityItems:@[[NSURL URLWithString:@"https://www.google.com"]] applicationActivities:nil];
  	[self presentViewController:shareController animated:YES completion:NULL];
  }]];
}
```
