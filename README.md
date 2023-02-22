# IDEMS JSXGRAPH Collaboration Repo
## Using this repo
To start a new project you should make a copy of the template and paste it in the relevant location. DO NOT modify or relocate the template. If you would like to create a personal folder please do so at the projects level. If you are starting a new project please create the relevant folder.

For individual projects you can committ directly to the master branch. For all collaborative projects, create a new brach and PR to update the repo.
## TODO
* Script to run through all files and change the version
* Script to select files to chage the version
## Useful considerations
### Previewing
You can view your JSXGraph by opening the file through a browser. If you make changes, you should save them and refresh the browser to see the changes. Recall that you can right-click on the file and reveal in file explorer to find it directly. 
## STACKifying
### Change 'jxgbox' to divid
```
        var board = JXG.JSXGraph.initBoard('jxgbox', {
```
should be 
```
        var board = JXG.JSXGraph.initBoard(divid, {
```
### JSXGRAPH Version
The version of JSXGraph used is defined in lines 9 and 10 in the template. Ensure you have the correct version set up. This is determined in your STACK installation. (If you create a jsxgraph with functions from newer versions they will not work when you transfer them to STACK.)
### Extracting answers 
Example 1:
There are 8 points that I'm evaluating in STACK so I define 8 input answers in the block 'opening' as follows
```
[[jsxgraph input-ref-ans1="sR1" input-ref-ans2="sR2" input-ref-ans3="sR3" input-ref-ans4="sR4" input-ref-ans5="sR5" input-ref-ans6="sR6" input-ref-ans7="sR7" input-ref-ans8="sR8"]]
```
I then bind the points to the answers as follows
```
/* Set answers from state of graph */
stack_jxg.bind_point(sR1,top_lq);
stack_jxg.bind_point(sR2,bot_lq);
stack_jxg.bind_point(sR3,top_med);
stack_jxg.bind_point(sR4,bot_med);
stack_jxg.bind_point(sR5,top_uq);
stack_jxg.bind_point(sR6,bot_uq);
stack_jxg.bind_point(sR7,mid_lq);
stack_jxg.bind_point(sR8,mid_uq);
board.unsuspendUpdate();
```
### Changing size
When creating the JSXGraph block in STACK you can define the dimensions of your box. For example:
```
[[jsxgraph height='100px' width='300px']]
```
will create a box of height 100px and width 300px.
## Useful links
* [JSXGraph webiste](https://jsxgraph.uni-bayreuth.de/wp/index.html)
* [JSXGraph wiki](https://jsxgraph.org/wiki/index.php/Main_Page) - Some guides and examples
* [JSXGraph documentation](https://jsxgraph.uni-bayreuth.de/docs/) - Full description of all objects and functions in the library
* [Google Group](https://groups.google.com/g/jsxgraph) - Community of developers and users where you can post questions
* [Sample STACK Question](https://ecampus.idems.international/question/bank/history/history.php?entryid=67010&returnurl=%2Fquestion%2Fedit.php%3Fcourseid%3D72%26cat%3D3445%252C7256%26qpage%3D0&courseid=72) - A STACK example of a question with a JSXGraph
