Bubble Sort Visualization
-------------------------
 
  The bubble sort. We compare K(1) with K(2), interchange R(1) with R(2) if the keys are out of order; then we do the same to R(2) and R(3), R(3) and R(4) etc. During this sequence of operations, records with large keys will move up. Repetitions of the process wil get the apropriate records into positions R(N), R(N-1), R(N-2) etc. so that all records will ultimately be sorted.
  The method is called bubble sorting because large elements bubble up to their proper position. After each pass through the file, it is not hard to see that all records above and including the last one to be exchanged must be in their final position, so they need not be examined on subsequence passes.

How it works!
------------

    from google.appengine.ext import webapp
    from google.appengine.ext.webapp import util
    from google.appengine.ext.webapp import template

    class MainHandler(webapp.RequestHandler):
       def get(self):
           self.response.out.write(template.render('bubblesort.html',''))


    def main():
           application = webapp.WSGIApplication([('/', MainHandler)],
                                     debug=True)
           util.run_wsgi_app(application)


    if __name__ == '__main__':
           main()


