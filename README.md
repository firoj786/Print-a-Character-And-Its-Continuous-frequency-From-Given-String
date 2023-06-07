# Print-a-Character-And-Its-Continuous-frequency-From-Given-String

package com.nt.important.java8;

import java.util.LinkedHashMap;

import java.util.Map;

/**
 * 
 * Print a character and its continuous frequency from given string.
 * 
 * String Input = "aabbbccddaaabbccceeff";
 * 
 *   String Output = a2b3c2d2a3b2c3e2f2
 * 
 * @author Firoj
 * 
 * @since 2022-01-05
 * 
 */
public class StringFiroj {

	public static void main(String[] args) {
  
			int count = 0;

		char tch = str.charAt(0);
		
		for (int i = 0; i < str.length(); i++) {
		
			char ch = str.charAt(i);
			
			if (ch == tch) {
			
				count++;
				
			} else {
			
				System.out.print(tch + "" + count + "");
				
				tch = ch;
				
				count = 1;

			}

		}
		
		System.out.print(tch + "" + count + "");

	}

	public static void main(String[] args) {
	
		String str = "aabbbccddaaabbccceeff";
		
		charFreqCount(str);
		
	}

}


