# Gallery-access-tool
from flask import Flask, render_template, url_for

app = Flask(__name__)

images = [
    {'src': 'image1.jpg', 'alt': 'Image 1'},
    {'src': 'image2.jpg', 'alt': 'Image 2'},
    {'src': 'image3.jpg', 'alt': 'Image 3'},
]

@app.route('/')
def home():
    return render_template('home.html', images=images)

if __name__ == '__main__':
    app.run(debug=True)
