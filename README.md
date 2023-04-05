# preorder

class Solution {
public:
    void preorder(TreeNode* root, vector<int> & vct){
       if(root==NULL){
           return ;
       }
       vct.push_back(root->val);
       preorder(root->left, vct);
       preorder(root->right , vct);
   }
    
    vector<int> preorderTraversal(TreeNode* root) {
        vector<int> vct;
        preorder(root, vct);
        return vct;
    }
};
