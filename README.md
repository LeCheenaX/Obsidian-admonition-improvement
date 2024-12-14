# Obsidian-admonition-improvement
Offers some improvements in styles for obsidian admonition plugin. 

## Issues in the default admonition style
### Inaccordance behavior of line-breaks under different mode
In reading view, the callout may behave like this: 

![image](https://github.com/user-attachments/assets/3d000efc-17b7-4d56-80bb-ea82342b7106)

However, when you switch to edit view:

![image](https://github.com/user-attachments/assets/17fb5281-29f6-49b5-ae5f-791bd6118498)

The line-breaks at the beginning is wrapped, while the line-breaks at the bottom is increased significantly. 

### Inaccordance of margins
To clarify, I will use "border" style in "Blue_Topaz" theme. This style is clearer to show the issue. 

![image](https://github.com/user-attachments/assets/eeca6f67-3166-425d-a3b3-ce7562b0b26b)

As is clearly shown above, the left/right margin is about 8px, while the top/bottom margin is 16px. 

I believe 8px for left margin looks good, and as right margin is not defined (automatically suits text), the top/bottom margin makes the paragraph look very uncomfortable. 

### Child callouts issue
In a very complicated case(just to show the issue), the spaces between child-callout and child-callout, between paragraph and child-callout seem very awful. The space is not coordinated. 
![image](https://github.com/user-attachments/assets/35a7b511-22c5-4c9c-8ec9-59565fc3dd27)


Moreover, consider writing the following paragraph in a child callout in source view: 
```
wohoo

wohoo
wohoo
```
In reading view, it seems fine as above screenshot shows. 

However, in live-preview, the line break is omitted (bug).
![image](https://github.com/user-attachments/assets/376af103-a6d6-4bc7-91a7-fe582e9843be)

## The workaround
The css snippets fixes the above issue by: 

1.making the callout contents exactly the same in reading view and live-preview, no inaccordance issue 

2.if deem contents in a callout as a whole:

	2.1 setting the margin of this whole to the same value
  
	2.2 preserving the margin of sub-contents in this whole
  
3.making child callouts behave the same like normal callout, but more clean and organized

4.optimizing margin of paragraph with bullet list and number list

Now the previous complicated case looks very fine:
![image](https://github.com/user-attachments/assets/e7866cef-b599-4422-9d1c-119450c8e9c5)

## More examples 
Before:

![image](https://github.com/user-attachments/assets/362dd7d3-0cb5-4915-8a4f-71979b440d22)

After: 

![image](https://github.com/user-attachments/assets/a3450715-2624-4c23-877c-e134e47058a0)


---

Before:

![image](https://github.com/user-attachments/assets/a74551ec-ba2c-4df7-b2ae-af98b9fd6802)

After: 

![image](https://github.com/user-attachments/assets/c533ba8b-23de-49d3-bbd7-a56484fa4504)

---

Before:

![image](https://github.com/user-attachments/assets/387a0944-5b47-49c1-91bd-0dd94812c408)

After:

![image](https://github.com/user-attachments/assets/51bf4eb5-1801-49d0-bd68-d028ab515584)



