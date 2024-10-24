# C-
676.IMD
class MagicDictionary {
public:
    vector<string> a;
    MagicDictionary() {
        
    }
    
    void buildDict(vector<string> dictionary) {
        for(int i=0;i<dictionary.size();i++){
            a.push_back(dictionary[i]);
        }
    }
    
    bool search(string searchWord) {
        int f=0;
        for(int i=0;i<a.size();i++){
            string temp=a[i];
            if(a[i].size()!=searchWord.size())  continue;
            int curr=0;
            for(int j=0;j<temp.size();j++){
                if(temp[j]==searchWord[j])  curr++;
            }
            if(curr==temp.size()-1){
                f=1;
                break;
            }
        }

        return f==1;
    }
};

/**
 * Your MagicDictionary object will be instantiated and called as such:
 * MagicDictionary* obj = new MagicDictionary();
 * obj->buildDict(dictionary);
 * bool param_2 = obj->search(searchWord);
 */
