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
  
		String Input = "aabbbccddaaabbccceeff";

		String input = "aabbbccddaaabbccceeff";

        Map<Character, Integer> frequencyMap = new LinkedHashMap<>();

        char[] chars = input.toCharArray();
        
        int count = 1;
        
        for (int i = 0; i < chars.length; i++) {
        
            if (i + 1 < chars.length && chars[i] == chars[i + 1]) {
            
                count++;
                
            } else {
            
                frequencyMap.put(chars[i], count);
                
                count = 1;
            }
        }

        StringBuilder output = new StringBuilder();
        
        for (Map.Entry<Character, Integer> entry : frequencyMap.entrySet()) {
        
            output.append(entry.getKey()).append(entry.getValue());
            
        }

        System.out.println(output);
	}

}


