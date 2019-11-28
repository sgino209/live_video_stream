(*) Switch for VirtualEnv:
    % bash
    % virtualenv -p $(which python3) venv
    % source venv/bin/activate
    end with:  deactivate

(*) Deploy on Heroku server (with Heroku CLI, assuming app is already in some Git repo):
    Reference:  https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Deployment
    % heroku login
    % heroku create
    % git push heroku master
    % heroku open

(*) Add a Heroku app as a Git remote:
    % heroku git:remote -a app

(*) Check the add-ons to the app:
    % heroku addons

(*) Check the configutarion variables:
    % heroku config

(*) Set configutarion variables:
    % heroku config:set VARIABLE=<value>

(*) Heroku app info:
    % heroku pg:info

(*) Heroku database reset (be careful..):
    % heroku pg:reset DATABASE [--confirm app]

(*) Heroku app restart:
    % heroku restart

(*) Update local git and deploy to Git and to Heroku server:
    % git add <files>
    % git commit -m '<comment>'
    % git push origin master
    % git push heroku master
    
(*) Debug with Heroku CLI:
    % heroku logs                              ---> Show current logs
    % heroku logs --tail                       ---> Show current logs and keep updating with any new results
    % heroku config:set DEBUG_COLLECTSTATIC=1  ---> Add additional logging for collectstatic (this tool is run automatically during a build)
    % heroku ps                                ---> Display dyno status

(*) Connect to Heroku shell:
    % heroku run bash
    % ...
    % exit

(*) Heroku CLI update:
    % heroku update

(*) Heroku Automated Certification Management (requires Hobby+ plan):
    % heroku certs:auto:enable   ---> Enable
    % heroku certs:auto          ---> Check status

