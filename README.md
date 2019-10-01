# compress_string

package elclipse;
import java.util.*;
public class compress_string {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

		String s="aaaabbbjjipa";                      


		String ouptut=compress(s);
		System.out.print(ouptut);
	}
	public static String compress(String s) {
		int count=1;
		String out="";

		for(int i=0;i<s.length();i++) {
			if(i!=s.length()-1 && s.charAt(i)==s.charAt(i+1)) {            ///checking the conditons
				count++;
				continue;
			}
			else if(count==1) {
				out=out+s.charAt(i);
			}
			else {
				out =out +s.charAt(i)+count;
				count=1;
			}
		}
		return out;

	}
}


/////time complexity is O(N).
