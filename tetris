import random 
import tkinter

fieldSize = 25  #盤面を描画
fieldWidth = 10
fieldHeight = 20
moveRight = 0
moveLeft = 1
moveDown = 2

class BlockType:
    def __init__(self, cell):
        self.mino = ["tag1","tag2","tag3","tag4"]
        self.cell = cell
#ミノの設定
    def gen(self):
        a = random.randrange(0,7)   #ミノをランダムに出現させる
        self.cnt = 0
        if a == 0:  #I
            self.block = [[4,0,"tag1"], [4,-1,"tag2"], [4,-2,"tag3"], [4,-3,"tag4"]]
            self.round = [{"tag1": [1, -1], "tag2": [0, 0], "tag3": [-1, 1], "tag4": [-2, 2]},
                {"tag1": [-1, 1], "tag2": [0, 0], "tag3": [1, -1], "tag4": [2, -2]},]
            self.mino["bg"] = "#87CEEB"
        elif a == 1:    
            self.block = [[4, 0, "tag1"], [4, -1, "tag2"], [3, -1, "tag3"], [5, -1, "tag4"]]
            self._round = [
                {"tag1": [1, -1], "tag2": [0, 0], "tag3": [1, 1], "tag4": [-1, -1]},
                {"tag1": [-1, -1], "tag2": [0, 0], "tag3": [1, -1], "tag4": [-1, 1]},
                {"tag1": [-1, 1], "tag2": [0, 0], "tag3": [-1, -1], "tag4": [1, 1]},
                {"tag1": [1, 1], "tag2": [0, 0], "tag3": [-1, 1], "tag4": [1, -1]},
            ]
            self.mino["bg"] = "#FFD700"
        elif a == 2:
            self.block = [[4, 0, "tag1"], [3, 0, "tag2"], [4, -1, "tag3"], [3, -1, "tag4"]]
            self._round = [
                {"tag1": [0, 0], "tag2": [0, 0], "tag3": [0, 0], "tag4": [0, 0]},
            ]
            self.mino["bg"] = "#008000"
        elif a == 3:
            self.block = [[4, 0, "tag1"], [4, -1, "tag2"], [5, -1, "tag3"], [5, -2, "tag4"]]
            self._round = [
                {"tag1": [0, 0], "tag2": [0, 0], "tag3": [-2, 0], "tag4": [0, 2]},
                {"tag1": [0, 0], "tag2": [0, 0], "tag3": [2, 0], "tag4": [0, -2]},
            ]            
            self.mino["bg"] = "#FF0000"

        elif a == 4:
            self.block = [[4, 0, "tag1"], [4, -1, "tag2"], [3, -1, "tag3"], [3, -2, "tag4"]]
            self._round = [
                {"tag1": [0, -2], "tag2": [0, 0], "tag3": [0, 0], "tag4": [2, 0]},
                {"tag1": [0, 2], "tag2": [0, 0], "tag3": [0, 0], "tag4": [-2, 0]},
            ]            
            self.mino["bg"] = "#4169E1"

        elif a == 5:
            self.block = [[4, 0, "tag1"], [4, -1, "tag2"], [4, -2, "tag3"], [3, -2, "tag4"]]
            self._round = [
                {"tag1": [0, 0], "tag2": [0, 0], "tag3": [-2, 2], "tag4": [0, 2]},
                {"tag1": [0, 0], "tag2": [0, 0], "tag3": [2, -2], "tag4": [2, 0]},
                {"tag1": [0, 0], "tag2": [0, 0], "tag3": [2, 1], "tag4": [0, -1]},
                {"tag1": [0, 0], "tag2": [0, 0], "tag3": [-2, -1], "tag4": [-2, -1]},
            ]            
            self.mino["bg"] = "#FF8C00"

        else:
            self.block = [[4, 0, "tag1"], [4, -1, "tag2"], [4, -2, "tag3"], [5, -2, "tag4"]]
            self._round = [
                {"tag1": [-1, -2], "tag2": [0, 0], "tag3": [0, 0], "tag4": [-3, 0]},
                {"tag1": [0, 1], "tag2": [0, 0], "tag3": [0, 0], "tag4": [2, -1]},
                {"tag1": [2, 0], "tag2": [0, 0], "tag3": [0, 0], "tag4": [2, 2]},
                {"tag1": [1, -1], "tag2": [0, 0], "tag3": [0, 0], "tag4": [-1, -1]}]
            self.mino["bg"] = "#8A2BE2"

            for i in range(len(self._round)):
                for tag in self.tags:
                    for n in range(2):
                        self._round[i][tag][n] = self._round[i][tag][n]*self.cell

                return self.block
