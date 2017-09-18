# Entertainment_center

import media
import fresh_tomatoes

avatar = media.movie("Avatar","A marine on an alien planet",
                     "https://upload.wikimedia.org/wikipedia/en/thumb/b/b0/Avatar-Teaser-Poster.jpg/220px-Avatar-Teaser-Poster.jpg"
                     ,"http://www.iqiyi.com/v_19rrn8vkts.html")

school_of_rock = media.movie("School_of_Rock","Using rock music to learn",
                             "https://upload.wikimedia.org/wikipedia/en/1/11/School_of_Rock_Poster.jpg",
                             "http://www.iqiyi.com/v_19rrk2xb94.html")

ratatouille = media.movie("Ratatouille","A rat is a chef in Paris",
                          "https://upload.wikimedia.org/wikipedia/en/5/50/RatatouillePoster.jpg",
                          "http://www.iqiyi.com/v_19rrifmczd.html")

movies = [avatar,school_of_rock,ratatouille]

fresh_tomatoes.open_movies_page(movies)

avatar.show_trailer()
school_of_rock.show_trailer()
ratatouille.show_trailer()

#media
import webbrowser

class movie():
    def __init__(self,movie_title,movie_storyline,poster_image,trailer_url):
        self.title = movie_title
        self.storyline = movie_storyline
        self.poster_image_url = poster_image
        self.trailer_youtube_url = trailer_url

    def show_trailer(self):
        webbrowser.open(self.trailer_youtube_url)
