# 第四次实验
实验四 字符串实验

一。实验目的：

1.掌握字符串String及其方法的使用

2.掌握异常处理结构

二。业务要求
内容：利用已学的字符串处理知识编程完成《长恨歌》古诗的整理对齐工作，写出功能函数，并运行。达到如下功能：

1.每7个汉字加入一个标点符号，奇数时加“，”，偶数时加“。”

2.允许提供输入参数，统计古诗中某个字或词出现的次数

3.考虑操作中可能出现的异常，在程序中设计异常处理程序


三。实验过程

通过分析实验要求，设计了三块代码：
1.分词+加标点（换行）
2.统计词频
3.异常处理
1.分词+加标点（换行）
把一大段文字切分成每七个字一组，在每组之后判断是加“，”还是加“。”和换行
2.统计词频
输入一个字符串，在原文本之中查找出现了几次并输出出现次数
3.异常处理
异常处理设计在了统计词频之后。如果统计词频这块的代码出现了问题，就会输出“程序查找过程出现错误”

四。实验流程图

见附件 流程图

五。代码

package Gushi;
import java.util.Scanner;
public class gushi {
	public static void main(String[] args) {
		StringBuffer shige=new StringBuffer("汉皇重色思倾国御宇多年求不得杨家有女初长成养在深闺人未识天生丽质难自弃一朝选在君王侧回眸一笑百媚生六宫粉黛无颜色春寒赐浴华清池温泉水滑洗凝脂侍儿扶起娇无力始是新承恩泽时云鬓花颜金步摇芙蓉帐暖度春宵春宵苦短日高起从此君王不早朝承欢侍宴无闲暇春从春游夜专夜后宫佳丽三千人三千宠爱在一身金屋妆成娇侍夜玉楼宴罢醉和春姊妹弟兄皆列土可怜光彩生门户遂令天下父母心不重生男重生女骊宫高处入青云仙乐风飘处处闻缓歌慢舞凝丝竹尽日君王看不足渔阳鼙鼓动地来惊破霓裳羽衣曲九重城阙烟尘生千乘万骑西南行翠华摇摇行复止西出都门百余里六军不发无奈何宛转蛾眉马前死花钿委地无人收翠翘金雀玉搔头君王掩面救不得回看血泪相和流黄埃散漫风萧索云栈萦纡登剑阁峨嵋山下少人行旌旗无光日色薄蜀江水碧蜀山青圣主朝朝暮暮情行宫见月伤心色夜雨闻铃肠断声天旋地转回龙驭到此踌躇不能去马嵬坡下泥土中不见玉颜空死处君臣相顾尽沾衣东望都门信马归归来池苑皆依旧太液芙蓉未央柳芙蓉如面柳如眉对此如何不泪垂春风桃李花开日秋雨梧桐叶落时西宫南内多秋草落叶满阶红不扫梨园弟子白发新椒房阿监青娥老夕殿萤飞思悄然孤灯挑尽未成眠迟迟钟鼓初长夜耿耿星河欲曙天鸳鸯瓦冷霜华重翡翠衾寒谁与共悠悠生死别经年魂魄不曾来入梦临邛道士鸿都客能以精诚致魂魄为感君王辗转思遂教方士殷勤觅排空驭气奔如电升天入地求之遍上穷碧落下黄泉两处茫茫皆不见忽闻海上有仙山山在虚无缥渺间楼阁玲珑五云起其中绰约多仙子中有一人字太真雪肤花貌参差是金阙西厢叩玉扃转教小玉报双成闻道汉家天子使九华帐里梦魂惊揽衣推枕起徘徊珠箔银屏迤逦开云鬓半偏新睡觉花冠不整下堂来风吹仙袂飘飖举犹似霓裳羽衣舞玉容寂寞泪阑干梨花一枝春带雨含情凝睇谢君王一别音容两渺茫昭阳殿里恩爱绝蓬莱宫中日月长回头下望人寰处不见长安见尘雾惟将旧物表深情钿合金钗寄将去钗留一股合一扇钗擘黄金合分钿但教心似金钿坚天上人间会相见临别殷勤重寄词词中有誓两心知七月七日长生殿夜半无人私语时在天愿作比翼鸟在地愿为连理枝天长地久有时尽此恨绵绵无绝期 ");
    //new StringBuffer内写的是您想要转换格式的诗歌
		for(int index=0;index<shige.length();index++) {
			if(index%8==0) {
				shige.insert(index,"\n");
			}
		}
		System.out.println(shige.toString());
		for(int n=8;n<shige.length();n=n+9) {
			shige.insert(n,"，");	
		}
		for(int m=17;m<shige.length();m=m+19) {
			shige.insert(m,"。");					
		}
		for(int p=18;p<shige.length();p=p+18) {
			shige.deleteCharAt(p);					
		}
		System.out.println(shige);			
	    Scanner scan = new Scanner(System.in);
	    String str = new String("汉皇重色思倾国御宇多年求不得杨家有女初长成养在深闺人未识天生丽质难自弃一朝选在君王侧回眸一笑百媚生六宫粉黛无颜色春寒赐浴华清池温泉水滑洗凝脂侍儿扶起娇无力始是新承恩泽时云鬓花颜金步摇芙蓉帐暖度春宵春宵苦短日高起从此君王不早朝承欢侍宴无闲暇春从春游夜专夜后宫佳丽三千人三千宠爱在一身金屋妆成娇侍夜玉楼宴罢醉和春姊妹弟兄皆列土可怜光彩生门户遂令天下父母心不重生男重生女骊宫高处入青云仙乐风飘处处闻缓歌慢舞凝丝竹尽日君王看不足渔阳鼙鼓动地来惊破霓裳羽衣曲九重城阙烟尘生千乘万骑西南行翠华摇摇行复止西出都门百余里六军不发无奈何宛转蛾眉马前死花钿委地无人收翠翘金雀玉搔头君王掩面救不得回看血泪相和流黄埃散漫风萧索云栈萦纡登剑阁峨嵋山下少人行旌旗无光日色薄蜀江水碧蜀山青圣主朝朝暮暮情行宫见月伤心色夜雨闻铃肠断声天旋地转回龙驭到此踌躇不能去马嵬坡下泥土中不见玉颜空死处君臣相顾尽沾衣东望都门信马归归来池苑皆依旧太液芙蓉未央柳芙蓉如面柳如眉对此如何不泪垂春风桃李花开日秋雨梧桐叶落时西宫南内多秋草落叶满阶红不扫梨园弟子白发新椒房阿监青娥老夕殿萤飞思悄然孤灯挑尽未成眠迟迟钟鼓初长夜耿耿星河欲曙天鸳鸯瓦冷霜华重翡翠衾寒谁与共悠悠生死别经年魂魄不曾来入梦临邛道士鸿都客能以精诚致魂魄为感君王辗转思遂教方士殷勤觅排空驭气奔如电升天入地求之遍上穷碧落下黄泉两处茫茫皆不见忽闻海上有仙山山在虚无缥渺间楼阁玲珑五云起其中绰约多仙子中有一人字太真雪肤花貌参差是金阙西厢叩玉扃转教小玉报双成闻道汉家天子使九华帐里梦魂惊揽衣推枕起徘徊珠箔银屏迤逦开云鬓半偏新睡觉花冠不整下堂来风吹仙袂飘飖举犹似霓裳羽衣舞玉容寂寞泪阑干梨花一枝春带雨含情凝睇谢君王一别音容两渺茫昭阳殿里恩爱绝蓬莱宫中日月长回头下望人寰处不见长安见尘雾惟将旧物表深情钿合金钗寄将去钗留一股合一扇钗擘黄金合分钿但教心似金钿坚天上人间会相见临别殷勤重寄词词中有誓两心知七月七日长生殿夜半无人私语时在天愿作比翼鸟在地愿为连理枝天长地久有时尽此恨绵绵无绝期");
	    Scanner scan1 = new Scanner(System.in);
	    System.out.println("请输入你要查找的子字符串：");
	    String a = scan1.nextLine();
	    int count = 0;
	    int start = 0;
	    try {
	    	while (str.indexOf(a, start) >= 0 && start < str.length()) {
	    		count++;
	    		start = str.indexOf(a, start) + a.length();
	    	}
	    	System.out.println(a  + "出现的次数为:" + count);
	  	}
	    catch(Exception Exception) {
			System.out.println("程序查找过程出现错误");
	    }
	}
}

六。程序运行截图
见附件 --“微信截图.......”

七。编程感想
    这次实验运用了对于字符串的各种操作，还尝试了异常程序处理。这次实验对于已经学过Python相关内容的我来说鼻前几次的实验都相对简单，但是这次提交报告的方式特别新颖，用了GitHub这个以前我从未接接触过的平台，让我更加认识到程序员的世界到底是多么的广阔。
    这次实验对于我来说还是有不足的地方：比如说上传Java文件时遇到了很多意想不到的问题，但是晚上宿舍断电并不足以支持我把这个问题解决，是这次实验的不足之处。下次实验我会好好解决这个提交文件的问题的。
