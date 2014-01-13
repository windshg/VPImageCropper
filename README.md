VPImageCropper
==============

That was a long night. I feel lonely and horny. Then I try to find something to do. I took out my iPhone and open WeChat, I check the messages and glance over the Friends Circle. I also try to upload my new portrait then I found the image cropper in WeChat was kind of funny. Out of nowhere, I decided to write a toy analogously instead of watching porn. All right, just skip all this crap and go to the point.

##Usage
It's just bloody easy to use this kit. Before present the cropper view controller, you should implement the protocol ``VPImageCropperDelegate``:

```ObjectiveC
// callback when cropping finished
- (void)imageCropper:(VPImageCropperViewController *)cropperViewController didFinished:(UIImage *)editedImage;

// callback when cropping cancelled
- (void)imageCropperDidCancel:(VPImageCropperViewController *)cropperViewController;
```

Now it's time to present the image cropper view controller and do some cropping.
```ObjectiveC
// present the cropper view controller
VPImageCropperViewController *imgCropperVC = [[VPImageCropperViewController alloc] initWithImage:portraitImg cropFrame:CGRectMake(0, 100.0f, self.view.frame.size.width, self.view.frame.size.width) limitScaleRatio:3.0];
imgCropperVC.delegate = self;
[self presentViewController:imgCropperVC animated:YES completion:^{
        // TO DO
}];
```

##Summary
As negligible as it is, I am glad this work could be used in some of the products in our company which is the best part. Anyway, if you are interested enough to have a test. Please refer to the VPImageCropperDemo Project and enjoy the beauty of coding.
