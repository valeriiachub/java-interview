## Write a method which will determine whether or not the string has duplicate characters?
**Solution**   

    public boolean checkIfAllCharactersUnique(String str) {
        char[] chars = str.toCharArray();
    
        for(Character ch : chars) {
            if(!(str.indexOf(ch) == str.lastIndexOf(ch))) {
                return true;
            }
        }
    
        return false;
    }
