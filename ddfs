from PyQt5.QtCore import Qt
from random import randint

class Question():
    def __init__(self,question,answer,wrong_answer1,wrong_answer2, wrong_answer3,attempts,correct):
        self.question = question
        self.answer = answer
        self.wrong_answer1 = wrong_answer1
        self.wrong_answer2 = wrong_answer2
        self.wrong_answer3 = wrong_answer3
        self.is_active = True
        self.attempts = 0
        self.correct = 0
    def got_right(self):
        self.attemts +=1
        self.correct +=1

    def got_wrong(self):
        self.attemps += 1

class QuestionView():
    def __init__(self, frm_model, question, answer,wrong_answer1, wrong_answer2, wrong_answer3):
        self.answer = answer
        self.question = question
        self.wrong_answer1 = wrong_answer1
        self.wrong_answer2 = wrong_answer2
        self.wrong_answer3 = wrong_answer3

    def  change(self, frm_model):
        self.frm_model = frm_model

    def show(self):
        self.question.setText(self,frm_model.question)
        self.answer.setText(self,frm_model.answer)
        self.wrong_answer1.setText(self.frm_model.wrong_answer1)
        self.wrong_answer2.setText(self.frm_model.wrong_answer2)
        self.wrong_answer3.setText(self.frm_model.wrong_answer3)


class QuestionEdit(QuestionView):
    def save_question(self):
        self.frm_model.question = self.question.text()

    def save_answer(self):
        self.frm_model.model.wrong_answer1 = self.wrong_answer1.text()
        self.frm_model.model.wrong_answer2 = self.wrong_answer2.text()
        self.frm_model.model.wrong_answer3 = self.wrong_answer3.text()

    def set_connects(self):
        self.question.editingFinished.connect(self.save_question)
        self.answer.editingFinished.connect(self.save_answer)
        self.wrong_answer1.editingFinished.connect(self.save_wrong)
        self.wrong_answer2.editingFinished.connect(self.save_wrong)
        self.wrong_answer3.editingFinished.connect(self.save_wrong)

    def __init__(self, frm_model, question, answer,wrong_answer1, wrong_answer2, wrong_answer3):
        QuestionView.__init__(self,self, frm_model = frm_model, question = question, answer = answer,wrong_answer1 = wrong_answer1, wrong_answer2 = wrong_answer2, wrong_answer3 = wrong_answer3 )



        self.set_connects()

class AnswerCheck(QuestionView):
    def __init__(self, frm_model, qustion, answer, wrong_answer1, wrong_answer2, wrong_answer3, showed_answer, result):
        QuestionView.__init__(self, self, frm_model=frm_model, question=question, answer=answer,
                              wrong_answer1=wrong_answer1, wrong_answer2=wrong_answer2, wrong_answer3=wrong_answer3)
        self.showed_aswer = showed_aswer
        self.result = result

class QuestionListModel (QAbstractListModel):
    def __init__(self, parent=None):
        QAbstractListModel.__init__(self,perent)
        self.from_list  = []

    def rowCount(self, index):
        return len(self.from_list)

    def date(self, index, role):
        if role == Qt.DisplayRole:
            from = self.from_list[index_role()]
            return 
