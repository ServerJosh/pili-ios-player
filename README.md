# PLPlayerKit

PLPlayerKit is set to play the live stream SDK is ** pili streaming cloud service ** offer aimed at resolving iOS end quickly and easily iOS devices to play live streaming, ease ** pili streaming cloud service developers ** focus on product business itself, without having to spend unnecessary time on the technical details.


## abstract

- [1 Quick Start] (# 1 - Quick Start)
- [1.1 Configuration Engineering] (# 1.1 Configuration Engineering)
- [1.2 sample code] (# 1.2 code sample)
- [2 third-party libraries] (# 2 - third-party libraries)
- [3 System Requirements] (# 3 - system requirements)
- [4 version history] (# 4 - version history)

## 1 Quick Start

### 1.1 Configuration Engineering

- Configure your Podfile file, add the following configuration information

`` `
pod 'PLPlayerKit', '1.0.1'
`` `

- Installation CocoaPods dependent

`` `
pod install
`` `

-! Done to run your project workspace

### 1.2 Sample Code

Add where needed

`` `Objective-C
#import <PLPlayerKit / PLPlayerKit.h>
`` `

initialization

`` `Objective-C
// Initialize VideoPlayerViewController
PLVideoPlayerViewController * viewPlayerViewController = [PLVideoPlayerViewController videoPlayerViewControllerWithContentURL: url parameters: parameters];

// Show player interface
[Self presentViewController: viewPlayerViewController animated: YES completion: nil];
`` `

Parameter Configuration

`` `Objective-C
NSMutableDictionary * parameters = [@ {} mutableCopy];

// For iPhone advised to turn off progressive scan, it is enabled by default
if (UI_USER_INTERFACE_IDIOM () == UIUserInterfaceIdiomPhone) {
parameters [PLMovieParameterDisableDeinterlacing] = @ (YES);
}
`` `

Playback operation, PLVideoPlayerViewController will automatically start playing when the show, of course, if you need to control their own play logic in the code, you can call the following method to easily start / pause
`` `Objective-C
// Play
[ViewPlayerViewController play];

// stop
[ViewPlayerViewController pause];
`` `

If you want to customize the player interface, then you need to hide the original playback control, you can do to

`` `Objective-C
viewPlayerViewController.controlMode = PLVideoPlayerControlModeNone;
`` `

## 2 third-party libraries included

- Ffmpeg

## 3 System Requirements

- IOS Target:> = iOS 6

## 4 Version History
- 1.0.1
- CocoaPods version initialize
- 1.0.0
- Complete the basic RTMP / HLS streaming player
