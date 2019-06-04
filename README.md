# 2nd-ML100Days
---------------------------------------------------------
def validation_int(n):
    if n.isdigit() == True and (1 <= int(n) <= 5):
        return True
    else:
        return False

import random
ans = random.randint(1, 5)
guess = [0]

for i in range(0, 1):
    a = input('請猜1到5的一個號碼: ')
    
    while validation_int(a) == False:
        a = input('請猜1到5的一個號碼: ')
        continue
    else:
        if int(a) != ans:
            print('wrong, answer is: ', ans)
        else:
            print('right, answer is: ', ans)            
----------------------------------------------------
import math

m = input('Please enter a number: ')
while m.isdigit() == False:
    m = input('You enter a float, please enter a int: ')
else:
    m = int(m)

a1 = []
for i in range(2, m+1):
    if i <= 3:
        a1.append(i)
    else:
        for j in range(2, int(math.sqrt(i))+1):
            if i%j == 0:
                break
        else:
            a1.append(i)

for i in a1:
    print('%d is prime' % i)
------------------------------------------------------------------------
def validation_int(n):
    if n.isdigit() == True and (1 <= int(n) <= 100):
        return True
    else:
        return False

import random
ans = random.randint(1, 100)
guess = [0]

while guess[-1] != ans:
    a = input('Please enter a int: ')

    while validation_int(a) == False:
        a = input('Out of range, please enter a int between 1~100: ')
        if validation_int(a) == False:
            continue
    else:
        a = int(a)
        guess.append(a)
        if a > ans:
            print('你這次猜%d, 你猜了%d次, 猜錯了，再小一點!' % (a, len(guess)-1))
        elif a < ans:
            print('你這次猜%d, 你猜了%d次, 猜錯了，再大一點!' % (a, len(guess)-1))
        else:
            print('你這次猜%d, 你猜了%d次, 猜對了!' % (a, len(guess)-1))
------------------------------------------------------------------------------------
a1 = "漢皇重色思傾國，御宇多年求不得。楊家有女初長成，養在深閨人未識。天生麗質難自棄，一朝選在君王側。回眸一笑百媚生，六宮粉黛無顏色。"\
     "春寒賜浴華清池，溫泉水滑洗凝脂。侍兒扶起嬌無力，始是新承恩澤時。雲鬢花顏金步搖，芙蓉帳暖度春宵。春宵苦短日高起，從此君王不早朝。"\
     "承歡侍宴無閒暇，春從春遊夜專夜。後宮佳麗三千人，三千寵愛在一身。金屋妝成嬌侍夜，玉樓宴罷醉和春。姊妹弟兄皆列土，可憐光彩生門戶。"\
     "遂令天下父母心，不重生男重生女。驪宮高處入青雲，仙樂風飄處處聞。緩歌慢舞凝絲竹，盡日君王看不足。漁陽鼙鼓動地來，驚破霓裳羽衣曲。"\
     "九重城闕煙塵生，千乘萬騎西南行。翠華搖搖行復止，西出都門百餘里。六軍不發無奈何，宛轉蛾眉馬前死。花鈿委地無人收，翠翹金雀玉搔頭。"\
     "君王掩面救不得，回看血淚相和流。黃埃散漫風蕭索，雲棧縈紆登劍閣。峨嵋山下少人行，旌旗無光日色薄。蜀江水碧蜀山青，聖主朝朝暮暮情。"\
     "行宮見月傷心色，夜雨聞鈴腸斷聲。天旋日轉迴龍馭，到此躊躇不能去。馬嵬坡下泥土中，不見玉顏空死處。君臣相顧盡沾衣，東望都門信馬歸。"\
     "歸來池苑皆依舊，太液芙蓉未央柳。芙蓉如面柳如眉，對此如何不淚垂。春風桃李花開日，秋雨梧桐葉落時。西宮南內多秋草，落葉滿階紅不掃。"\
     "梨園子弟白髮新，椒房阿監青娥老。夕殿螢飛思悄然，孤燈挑盡未成眠。遲遲鐘鼓初長夜，耿耿星河欲曙天。鴛鴦瓦冷霜華重，翡翠衾寒誰與共。"\
     "悠悠生死別經年，魂魄不曾來入夢。臨邛道士鴻都客，能以精誠致魂魄。為感君王輾轉思，遂教方士殷勤覓。排空馭氣奔如電，升天入地求之遍。"\
     "上窮碧落下黃泉，兩處茫茫皆不見。忽聞海上有仙山，山在虛無縹緲間。樓閣玲瓏五雲起，其中綽約多仙子。中有一人字太真，雪膚花貌參差是。"\
     "金闕西廂叩玉扃，轉教小玉報雙成。聞道漢家天子使，九華帳裏夢魂驚。攬衣推枕起徘徊，珠箔銀屏迤邐開。雲髻半偏新睡覺，花冠不整下堂來。"\
     "風吹仙袂飄颻舉，猶似霓裳羽衣舞。玉容寂寞淚闌干，梨花一枝春帶雨。含情凝睇謝君王，一別音容兩渺茫。昭陽殿裏恩愛絕，蓬萊宮中日月長。"\
     "回頭下望人寰處，不見長安見塵霧。唯將舊物表深情，鈿合金釵寄將去。釵留一股合一扇，釵擘黃金合分鈿。但教心似金鈿堅，天上人間會相見。"\
     "臨別殷勤重寄詞，詞中有誓兩心知。七月七日長生殿，夜半無人私語時。在天願作比翼鳥，在地願為連理枝。天長地久有時盡，此恨綿綿無絕期。"
     
a1_new = a1.replace('，', '')
a1_new = a1_new.replace('。', '')

a2 = list()
for i in a1_new:
    a2.append(a1_new.count(i))

print('長恨歌中出現最多次的字是"%s", 一共出現%d次' % (a1_new[a2.index(max(a2))], max(a2)))
print('扣掉標點符號後,長恨歌一共有%d個字' % (len(a1_new)))
--------------------------------------------------------------------------------------------------------------
mat_pass = {'柯南', '灰原', '步美', '美環', '光彥'}
eng_pass = {'柯南', '灰原', '丸尾', '野口', '步美'}

print('數學及格但英文不及格: %s' % (mat_pass.difference(eng_pass)))
print('英文及格但數學不及格: %s' % (eng_pass.difference(mat_pass)))
print('數學和英文都及格: %s' % (mat_pass.intersection(eng_pass)))

-------------------------------------------------------------------------------
