UIBarButtonItem-blocks
==================

***Category on UIBarButtonItem that implements block support***

This category adds block support for `UIBarButtonItem`.

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
