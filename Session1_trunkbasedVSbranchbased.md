
## Trunk-based Development vs Branch-based Development

### *1. Trunk-based Development*

* **Trunk**  
   * Trunk means main development branch under a version control system. It’s the base of a project, where all improvements are being merged together.


* **Continuous Integration**
  * Trunk-Based Development is a key enabler of Continuous Integration and by extension Continuous Delivery.  
  * When individuals on a team are committing their changes to the trunk multiple times a day it becomes easy to satisfy the core requirement of Continuous Integration that all team members commit to trunk at least once every 24 hours.    
  * This ensures the codebase is always releasable on demand and helps to make Continuous Delivery a reality.


* **Feature Toggles/Flags**
    * Trunk based Development and Feature Flags together can be used for continuous delivery, delivering the features faster to market.
    * Feature Toggles hide unfinished features behind flags that are turned off by default.
    * Developers can build a new feature by turning the flag off and deploying to master at any time, preventing merge conflicts before a new feature is completed.


1. **Work flow**
   1. Developer start works on the main branch or create a short-lived-feature branch (a branch from the trunk) and start work on them.      
   2. Once they are done with compiling and all testing, they push all changes to trunk (or merge to the trunk) directly (without making a pull request).   
   3. Optionally, open pull requests for short-lived-feature branches and each developer comment on changes and may have discussions and knowledge sharing.


2. **Pros**  
   1. Changes can be pushed to main line faster
   2. Update to project can be fast
   3. Minimum merge conflicts
   4. Very easy to hotfix production bugs
   5. CI/CD is very easy


3. **Cons**
    1. Breaking commits due to conflicts
    2. Less control over code
    3. Feature toggles are required

### *2. Branch-based Development*

* __Branch__  
  * Branches are created from the base project, in order to develop a new  feature, fix a bug, or simply do some refactoring.    
  * They prevent software  developers from disturbing each other and enable them to work in  parallel.    
  * Once a change is finished and tested, the branch is merged  back to the trunk.

* __Feature Branch__  
  * The feature branch has a clear and highly-focused purpose to add specific functionality to a project.   
  * It should not contain any other  changes that fix bugs, introduce other features, or are part of a  refactoring.
  
1. **Work Flow**
   1. Involves the use of feature branches and multiple primary branches. It has numerous, longer-lived branches and larger commits.
   2. Developers create a feature branch and delay merging it to the main trunk branch until the feature is complete.
   3. Once they are done, they create pull requests. In pull requests, each developer comment on changes and may have discussions. Once it’s agreed upon, the pull request is accepted and ready to be merged to the main branch.
   4. These long-lived feature branches require more collaboration to merge and have a higher risk of deviating from the trunk branch.
2. **Pros**

   1. Master branch is updated
   2. Feature toggles are not required
   3. Team size: no limit

3. **Cons**

   1. Difficult merge conflicts
   2. More deviation from merge branch
   3. Careful attention needs to be given to hotfix bugs
   4. CI/CD is difficult to maintain

    



### *Conclusion*
As a result, both methodologies have different advantages and disadvantages. So we need to decide a suitable methodology based on project requirement.