# Temperature-Convertor
from tkinter import *
from functools import partial

import random

class Convertor:
    def _init_(self):
        background_color = "light blue"
        self.convertor_frame = Frame(width=600, bg=background_color)
        self.convertor_frame.grid()
        self.temp_convertor_label = Label(self.convertor_frame, text="Temperature Convertor", font="Arial", "16", "bold", bg=background_color, padx=10, pady=10)
        self.temp_convertor_label.grid(row=0)
        self.help_button = Button(self.convertor_frame, text="help",padx=10,pady=10,command=self.help)
        self.help_button.grid(row=1)
        def help(self):
            print("You asked for help")
            get_help = Help(self)
            get_help.help_text.configure(test="Help text goes here")

  class Help:
    def_init_(self,partner):
    background = "orange"
    partner.help_button.config(state=DISABLED)

   self.help_box = Toplevel()
   self.help_box.protocol('WM_DELETE_WINDOW', partial(self.close_help_box))
   self.help_frame = Frame(self.help_box, bg=background)
   self.help_frame.grid()
   self.how_heading = Label(self.help_frame, text="Help / Instructions",font="arial 14 bold",bg=background)
   self.how_heading.grid(row=0)
   self.help_text = Label(self.help_frame, text="", justify=LEFT, width=40, bg=background)
   self.help_text.grid(row=1)
   self.dismiss_btn = Button(self.help_frame, text="Dismiss", width=10, bg="orange", font="arial", command=partial(self.close_help, partner))
   self.dismiss_btn.grid(row=2, pady=10)
   def close_help(selfself, partner):
     partner.help_button.config(state=NORMAL)
     self.help_box.destroy()



#main_routine
if _name_ == "_main_":
    root = Tk()
    root.title("Temperature Convertor")
    something = Convertor(root)
    root.mainloop()
