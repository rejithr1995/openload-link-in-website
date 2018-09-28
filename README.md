# openload-link-in-website
is their a way to automatically get the embed code and show the video URL in a website 


eg : if an embed video is showing in a page it has to get the video link from the embed code and show as download button below the video 


//Video ID
					if (preg_match('/f\'(.*?)\'/', $match, $matches_id)) {
						$video['id'] = trim($matches_id[1]);
					} else {
						if (!$this->debug) continue;
						else $debug_e[] = 'ID';
					}

//Embed Code
					$video['embed'] = '<iframe src="https://openload.co/embed/' . $video['id'] . 'scrolling="no" frameborder="0" width="700" height="430" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"></iframe>';
					if (already_added($video['embed'])) {
						++$this->video_already;
						continue;
					}
					
 //URL
					if(preg_match('/href=\'(.*?)\'/', $match, $matches_url)) {
						$video['url']   = 'https://openload.co'.$matches_url[1];
					} else {
						$this->errors[]	= 'Failed to get video URL for ID: '.$video['id'].'!';
						if (!$this->debug) continue;
						else $debug_e[] = 'URL';
					}





would this work ?
