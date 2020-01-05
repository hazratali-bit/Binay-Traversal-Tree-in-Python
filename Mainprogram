class BinaryTree:
    def __init__(self, data=None):
        self.data = data
        self.left = None
        self.right = None

    def set_root(self, data):
        self.data = data

    def inorder(self):
        if self.left is not None:
            self.left.inorder ()
        print (self.data, end=' ')
        if self.right is not None:
            self.right.inorder ()

    def preorder(self):
        print (self.data,end=' ')
        if self.left is not None:
            self.left.preorder()
        if self.right is not None:
            self.right.preorder()

    def postorder(self):
        if self.left is not None:
            self.left.postorder()
        if self.right is not None:
            self.right.postorder()
        print (self.data,end=' ')

    def insert_left(self, new_node):
        self.left = new_node

    def insert_right(self, new_node):
        self.right = new_node

    def search(self, data):
        if self.data == data:
            return self
        if self.left is not None:
            temp = self.left.search (data)
            if temp is not None:
                return temp
        if self.right is not None:
            temp = self.right.search (data)
            return temp
        return None


btree = None

print ('Menu (this assumes no duplicate keys)')
print ('insert <data> at root')
print ('insert <data> left of <data>')
print ('insert <data> right of <data>')
print ('quit')

while True:
    print ('inorder traversal of binary tree: ', end='')
    if btree is not None:
        btree.inorder ()
    print ()
    print ('preorder traversal of bianry tree: ',end='')
    if btree is not None:
        btree.preorder()
    print()
    print ('post order traversal of bianry tree:',end='')
    if btree is not None:
        btree.postorder()
    print()


    do = input ('What would you like to do? ').split ()

    operation = do[0].strip ().lower ()
    if operation == 'insert':
        dataa = int (do[1])
        new_node = BinaryTree (dataa)
        suboperation = do[2].strip ().lower ()
        if suboperation == 'at':
            btree = new_node
        else:
            position = do[4].strip ().lower ()
            data = int (position)
            ref_node = None
            if btree is not None:
                ref_node = btree.search (data)
            if ref_node is None:
                print ('No such key.')
                continue
            if suboperation == 'left':
                ref_node.insert_left (new_node)
            elif suboperation == 'right':
                ref_node.insert_right (new_node)

    elif operation == 'quit':
        break
