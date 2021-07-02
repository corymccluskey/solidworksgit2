#needed to run these commands to make git lfs happy
git lfs install
git config --global credential.helper cache
git config --global credential.helper wincred

#track certain types of files
git lfs track "*.sldprt"
git lfs track "*.docx"

#if failing to push
rm .git/hooks/pre-push
git push

ssh-keygen
eval $(ssh-agent)
copy .pub file contents and add key to bitbucket on website
ssh -T git@bitbucket.org
git config --global url.ssh://git@bitbucket.org/.insteadOf https://bitbucket.org/
