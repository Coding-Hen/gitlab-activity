# Gitlab Activity Stream Widget
This is a modified copy of the Github-activity by caseyscarborough (https://github.com/caseyscarborough/github-activity)

This is a small Javascript plugin that creates a stream of your recent Gitlab activity. It displays the user's name, username, photo, and a list of each individual activity type. Click [here](https://www.henry-slim.co.uk/gitlab-activity-demo) for a demo.

A sample image of the activity stream is shown below:

![](https://imgur.com/nIsK5ZS)

## Dependencies

The two dependencies for the plugin are the [Mustache](https://github.com/janl/mustache.js/) templating library and [Octicons](https://octicons.github.com/) (if you want the icons to show). You can include these along with the scripts for the plugin in the head of your page with the following HTML:

```html
<link rel="stylesheet" href="//cdnjs.cloudflare.com/ajax/libs/octicons/2.0.2/octicons.min.css">
<link rel="stylesheet" href="gitlab-activity.min.css">

<script type="text/javascript" src="//cdnjs.cloudflare.com/ajax/libs/mustache.js/0.7.2/mustache.min.js"></script>
<script type="text/javascript" src="gitlab-activity.min.js"></script>
```

The files can be downloaded from the [tags page](https://github.com/Coding-Hen/gitlab-activity/releases/tag).

If you'd like to build the files yourself:

```bash
# Ensure you have grunt and bower installed
npm install bower
npm install grunt-cli

# Clone the repository
git clone https://github.com/Coding-Hen/gitlab-activity.git
cd gitlab-activity

# Install dependencies
bower install

# Build dist
grunt
```

## Usage

To use the library, begin by creating a new div with an id in the body of your page:

```html
<div id="feed"></div>
```

Then call the feed method via Javascript:

```js
GitLabActivity.feed({
	username: "your-username",
	repository: "your-repo", // optional
	selector: "#feed",
	limit: 20 // optional
});
```

## Credits

* [MD5 Methods](http://www.myersdaily.org/joseph/javascript/md5-text.html)
* [Github-activity] (https://github.com/caseyscarborough/github-activity)
