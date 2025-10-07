/*
class Node {
    int data;
    Node left;
    Node right;

    Node(int data) {
        this.data = data;
        left = null;
        right = null;
    }
}
*/

class Solution {
    static class Pair {
        Node n;
        int hd;
        Pair(Node n, int hd) {
            this.n = n;
            this.hd = hd;
        }
    }
    
    public ArrayList<Integer> bottomView(Node root) {
        ArrayList<Integer> res = new ArrayList<>();
        if (root == null) return res;
        TreeMap<Integer, Integer> map = new TreeMap<>();
        Queue<Pair> q = new LinkedList<>();
        q.add(new Pair(root, 0));
        while (!q.isEmpty()) {
            Pair p = q.poll();
            map.put(p.hd, p.n.data);
            if (p.n.left != null) q.add(new Pair(p.n.left, p.hd - 1));
            if (p.n.right != null) q.add(new Pair(p.n.right, p.hd + 1));
        }
        res.addAll(map.values());
        return res;
   
    }
}
