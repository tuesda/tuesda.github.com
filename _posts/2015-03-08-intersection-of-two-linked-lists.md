---
layout: post
title: "intersection of two linked lists"
description: ""
category: algorithm
tags: [algorithm,java,oj]
---
{% include JB/setup %}

####问题####

题目链接见<https://oj.leetcode.com/problems/intersection-of-two-linked-lists/>   
Write a program to find the node at which the intersection of two singly linked lists begins.
```
A:          a1 → a2
                   ↘
                     c1 → c2 → c3
                   ↗            
B:     b1 → b2 → b3
```

如上，找出这两个链接的合并的地一个点c1    
节点定义：
```
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) {
 *         val = x;
 *         next = null;
 *     }
 * }
 */
 ```

####最初的思路####

用两个node分别同时迭代linkedA和linkedB，当这两个node的值相等，那么该节点就是我们要找的值

####缺陷####

没有考虑到linkedList长度不同的情况，

####最终方案####

解决两个链表长度不同的问题，很明显，链表后面是一样的，所以只要让链表在c1前面长度一样据可以了。具体来说就是把c1前长的链表多的地方截取掉。
