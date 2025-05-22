# Video on a Web Page Example
This is an example template file for how to show a video element on a web page.

1. **index.html** has a video elment in it already. You can upload your own video and then edit this element to show it.
    1. For the video element you have to upload your video file to the folder named __media__ for this one

## Instructions

For this you will edit index.html and upload your video to the media folder.

To use this template you will need to:

1. Upload your video file to the __media__ folder.
2. Edit __index.html__ to
   
	1. Change the src attribute in the source element. Also change the type if your video is not mp4
	2. Change the figcaption content to fit your video. If you made it then give yourself credit.
	3. Change all of the instances of YOUR_NAME in the header and footer.
	4. Change the text in the h1 from Your Project Name to your project's name.

7. Delete the instructions in index.html. You can also remove the content on this page by either removing or changing the README.md file.
8. [optional] You can also edit style.css and change the CSS to update the styling if you like (not required).
	
When you are editing source element for your video you will also need to make sure the **type** attribute is correct. This is a list of file types with the type attribute values. For most of you, the included example with type .mp4 will be fine. If you are including other types of videos here is a table of common types:
	

| File    | MIME Type attribute    |
|---------|------------|
| .mp4  | video/mp4   |
| .mpeg  | video/mpeg  |
| .webm  | video/webm  |
| .avi  | video/x-msvideo |
| .ogv  | video/ogg      |

For example
`<source src="videoFileName.mp4" type="video/mp4">`

You can see more here [https://developer.mozilla.org/en-US/docs/Web/HTTP/MIME_types/Common_types](https://developer.mozilla.org/en-US/docs/Web/HTTP/MIME_types/Common_types)

### Multiple video file types

You do not have to make multiple types of your video. If you do want to go the extra step and make sure that anyone can view your video you can save it as a few different file types and then upload all of these and have a source element for each. The browser will play the first file for which it has the right codec installed.

```
<video controls>
    <source src="media/filename.mp4" type="video/mp4">
    <source src="media/filename.webm" type="video/webm">
    <source src="media/filename.ogv" type="video/ogg">
</video>
```

### Note on .mov files
.mov is what is called a wrapper file type which means that it can have different types of video files inside of it. **The simplest and safest way to make sure your video plays in a broswer is to save it as .mp4 instead.** However, if you can't and have a .mov that uses the h.264 codec (a way of encoding a video file) then it _may_ play if you add it like this:

`<source src="videoFileName.mov" type="video/mp4">`

