# lca-of-binary-search-tree
todays task

class Solution {
    public TreeNode lowestCommonAncestor(TreeNode root, TreeNode p, TreeNode q) {
    int mini = Math.min(p.val, q.val);
        int maxi = Math.max(p.val, q.val);
        while (root != null) {
            if (root.val > maxi)
                root = root.left;
            else if (root.val < mini)
                root = root.right;
            else 
                return root;
        }
        return null;    
    }
}
