import time
import itchat

@itchat.msg_register(itchat.content.TEXT)
def tuling_reply(msg):
    if not msg['FromUserName'] == myUserName:
        #check if the message if sent from me
        itchat.send_msg(u"[%s]收到好友@%s 的信息： %s\n" %(time.strftime("%Y-%m-%d %H:%M:%S", time.localtime(msg['CreateTime'])),msg['User']['NickName'],msg['Text']), 'filehelper')
        #send the messages to file-helper for record
    return '[自动回复][捂脸]您好，我现在有事不在，一会儿再和您联系~ \n已经收到您的信息：%s\n' % (msg['Text'])
    #auto reply

if __name__ == '__main__':
    itchat.auto_login()
    myUserName = (itchat.search_friends()).get('UserName')
    #get my user name
    itchat.run()
