1.var gulp = require('gulp');
//gulp  Ĭ��ִ��
gulp.task('default', function() {
  ������
});

2.ִ��gulp,��������Ļ�������cmd�Թ���Ա������У���װgulp    npm install gulp --save-dev ���� modules

3.npm install ���� ֻ��npm install����ȫ����װ  gulp-sass ���ܻᰲװʧ�ܣ�Ȼ�󵥶����Ա�����װcnpm install gulp-sass���ɡ�
  node-sass  npm ���� please cnpm

-g��ȫ�ְ�װ�����ᰲװ��ȫ��·���£�����д��ϵͳ������������ֱ�۵ĸо����ǿ��Կ���ͨ�����������κεط���������ȫ��·�� ����npm config get prefix���Կ���·�����ҵ�ubuntuϵͳ��ʾ/usr/local/lib/node_modules/
��ȫ�ְ�װ�����ᰲװ�ڵ�ǰ��λĿ¼�� ���ذ�װ����װ�ڶ�λĿ¼��node_modules�ļ����£�ͨ��require()���ã�
--save��������������Ϣ��package.json��package.json��nodejs��Ŀ�����ļ�������Ϊnode���̫�࣬����һ��package�ļ���������Ϣ��֮��ά����������Ƚ��鷳
-dev��������package.json��devDependencies�ڵ㣬��ָ��-dev��������dependencies�ڵ㣻

��ȫ�ְ�װ��gulp������gulp -v ���Բ鿴gulp�汾��

4.����package.json���£�
npm init

npm install --save-dev gulp
npm install --save-dev gulp-autoprefixer //�Զ�ǰ׺

5.--save-dev�ĺô� ִֻ��npm install�Ļ���������package.json����devDependencies�е�ģ��ȫ����װ

6.gulp api

���ļ��Ͷ��ļ���д��

�ο���ַ��http://www.tuicool.com/articles/J3QnEb 

CSSѹ�����ϲ��ļ�

������ʾ��ִ��npm install cnpm -g --registry=https://registry.npm.taobao.org //�Ա����񡢹��ڵĿ��Ա�ø���

�򿪵�ip��һ���Ļ���һ�������߾�����ip,һ������̫��ip��������ip ����ͬ��

�����Զ�ˢ��Ԥ����Ҫ ��װ browser-sync��ͬʱ��������html�ṹ�в�����ʾ

�Զ�������ʧȥ�������Զ����档

ʹ��sass��ʱ��ע���β�Ĵ�����Ҫ���루��Ҫ��ֱ�Ӹ��ƹ����Ĵ��룩�������ױ���