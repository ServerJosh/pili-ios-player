PLPlayerKit is set to play the live stream SDK as pili streaming cloud services aimed at addressing iOS end quickly and easily iOS devices to play live streaming, ease of developers pili streaming cloud services focus on product business itself, rather than spending unnecessary time on the technical details.

abstract

1 Quick Start
1.1 Configuration Engineering
1.2 Sample Code
2 Third-party libraries
3 System Requirements
4 Version History
1 Quick Start

1.1 Configuration Engineering

Configure your Podfile file, add the following configuration information
pod 'PLPlayerKit', '1.0.1'
Installation CocoaPods dependence
pod install
Done! Run your project workspace
1.2 Sample Code

Add where needed

#import <PLPlayerKit / PLPlayerKit.h>
initialization

    // Initialize VideoPlayerViewController
    PLVideoPlayerViewController * viewPlayerViewController = [PLVideoPlayerViewController videoPlayerViewControllerWithContentURL: url parameters: parameters];

    // Show player interface
    [Self presentViewController: viewPlayerViewController animated: YES completion: nil];
Parameter Configuration

    NSMutableDictionary * parameters = [@ {} mutableCopy];

    // For iPhone advised to turn off progressive scan, it is enabled by default
    if (UI_USER_INTERFACE_IDIOM () == UIUserInterfaceIdiomPhone) {
        parameters [PLMovieParameterDisableDeinterlacing] = @ (YES);
    }
Playback operation, PLVideoPlayerViewController will automatically start playing when the show, of course, if you need to control their own play logic in the code, you can call the following method to easily start / pause

    // Play
    [ViewPlayerViewController play];

    // stop
    [ViewPlayerViewController pause];
If you want to customize the player interface, then you need to hide the original playback control, you can do to

    viewPlayerViewController.controlMode = PLVideoPlayerControlModeNone;
2 third-party libraries included

ffmpeg
3 System Requirements

iOS Target:> = iOS 6
4 Version History

1.0.1
CocoaPods version initialize
1.0.0
Complete basic RTMP / HLS streaming player
