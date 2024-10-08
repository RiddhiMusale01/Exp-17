# EXPERIMENT 17
# Aim 
# Theory
A linked list is a linear data structure made up of nodes linked together by pointers (in C or C++) or references (in Java, Python, and JavaScript). Each node contains data as well as a pointer/reference to the node immediately following it in the list. Unlike arrays, linked lists allow for efficient insertion or removal of elements from any position in the list because the nodes are not stored sequentially in memory.
```
#include <iostream>
using namespace std;

class Link {
public:
    int data;
    Link* next;

    Link(int num) {
        data = num;
        next = NULL;
    }
};

void insert_head(Link* &head, int data) {
    Link* new_node = new Link(data);
    new_node->next = head;
    head = new_node;
}

void disp(Link* head) {
    Link* temp = head;
    while (temp != NULL) {
        cout << temp->data << "->";
        temp = temp->next;
    }
    cout << "NULL" << endl;
}

int main() {
    Link* head = NULL;
    insert_head(head, 30);
    disp(head);
    insert_head(head, 32);
    disp(head);
    insert_head(head, 36);
    disp(head);
    return 0;
}

```
o/p:

![image](https://github.com/user-attachments/assets/edd58846-490d-43d2-9a5c-f9872f0adcfe)


```
#include <iostream>
using namespace std;

class Link {
public:
    int data;
    Link* next;

    Link(int num) {
        data = num;
        next = NULL;
    }
};

void insert_head(Link* &head, int data) {
    Link* new_node = new Link(data);
    new_node->next = head;
    head = new_node;
}

void delete_head(Link* &head){
    if(head!=NULL){
        Link* temp=head;
        head=head->next;
        delete temp;
    }
}
void disp(Link* head) {
    Link* temp = head;
    while (temp != NULL) {
        cout << temp->data << "->";
        temp = temp->next;
    }
    cout << "NULL" << endl;
}

int main() {
    Link* head = NULL;
    insert_head(head, 30);
    disp(head);
    insert_head(head, 32);
    disp(head);
    insert_head(head, 36);
    disp(head);
   
    delete_head(head);
    disp(head);
    return 0;
}
```
o/p:

![image](https://github.com/user-attachments/assets/9252861d-5774-46b1-bd46-7e772eb5f0d9)

# Conclusion
The code shows basic actions on a singly linked list, specifically the insertion and deletion of the head node. By combining these operations with a display function, the program clearly shows how to dynamically manipulate linked lists in memory.
