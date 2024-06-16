#!/bin/python3
from __future__ import unicode_literals
from colorama import Fore, Style
import yt_dlp
import ffmpeg
import sys
import os

ydl_opts = {
	'format': 'bestaudio/best',
#	'outtmpl': 'output.%(ext)s',
	'postprocessors': [{
		'key': 'FFmpegExtractAudio',
		'preferredcodec': 'wav',
	}],
}
def dl(url, name):
	ydl.download([url])
	os.system(f'mv *.wav downloaded/{name}.wav')


with yt_dlp.YoutubeDL(ydl_opts) as ydl:
	f=open('ytdl.txt','r')
	while True:
		data=f.readline()
		if data=='\n': break
		name, url=data.split(' : ')
		print(Fore.RED, f'\nDownloading {name}')
		print(Style.RESET_ALL)
		name=list(name)
		for i in range(len(name)):
			if name[i]==" ": name[i]="\\ "
		name="".join(name)
		print(name)
		dl(url, name)
