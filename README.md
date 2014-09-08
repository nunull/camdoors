# Bash functions

**.profile**

	cdclone() {
		echo "Changing into \"~/Desktop\""
		cd ~/Desktop

		if [ -d camdoors ]
		then
			echo "Removing \"~/Desktop/camdoors\""
			rm -r camdoors
		fi

		git clone https://github.com/nunull/camdoors.git camdoors
	}

	cdchrome() {
		/Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --use-fake-ui-for-media-stream &
	}

	cdserve() {
		if [ -d ~/Desktop/camdoors ]
		then
			echo "Changing into \"~/Desktop/camdoors\""
			cd ~/Desktop/camdoors
			./serve
		else
			echo "\"~/Desktop/camdoors\" does not exist. Use \"cdclone\""
		fi
	}