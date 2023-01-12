class Solution {
public:
    void helper(TreeNode* root, vector<int>& ans){
        if (root==NULL)return;
        helper(root->left,ans);   // left traversal
        ans.push_back(root->val); // store the root element
        helper(root->right,ans); // right traversal
    }
    void merge(vector<int>& v1, vector<int>& v2, vector<int>& ans){ // basic merge function
        int i=0, j=0;
        while (i<v1.size() && j<v2.size()){
            if (v1[i]<= v2[j]){
                ans.push_back(v1[i++]);
            }
            else ans.push_back(v2[j++]);
        }
        while (i<v1.size())ans.push_back(v1[i++]);
        while (j<v2.size())ans.push_back(v2[j++]);
        
    }
    vector<int> getAllElements(TreeNode* root1, TreeNode* root2) {
        vector<int> res;
        vector<int> vec1,vec2; // we make two temp vectors to store the tree's values in sorted fashion(inorder traversal of bst gives ascending order elements)
        helper(root1,vec1); // traverse over tree1
        helper(root2,vec2); // traverse over tree2
        merge(vec1,vec2,res); // merger vec1, vec2 into 'res'
        return res;
    }
};
