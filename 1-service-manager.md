** Default Services ** Defined in Zend\Mvc\Service

1. Zend\Mvc\Application is created
2. Zend\ServiceManager\ServiceManager object is created and configured by Zend\Mvc\Service\ServiceManagerConfig
Zend\ServiceManagerConfig get configuration from application.config.php

3. From all the service and factories provided in the Zend\Mvc\Service namespace, ServiceManagerConfig is responsible of configuring only three: SharedEventManager, EventManager, and ModuleManager

4. After this, the Application calls for the ModuleManager. At this point, the ModuleManager further configures the ServiceManager with services and factories provided in Zend\Mvc\Service\ServiceListenerFactory. 



A Zend\ServiceManager\ServiceManager is an implementation of Zend\ServiceManager\ServiceLocatorInterface. Its task is to provide
a service or retrieving other objects based on the service name.

*ServiceLocatorInterface*

namespace Zend\ServiceManager

public interface ServiceLocatorInterface
{
public function get ($name);
public function has($name);
}

In addition of implementing the above inteface, a Zend\ServiceManager\ServiceManager provides following addition API

*Service Registraion *
*Lazy-loaded Service Objects*
*Service Factories *
*Service Aliasing *
*Abstract Factories *
*Initializers *


***Service Manager Configuration***
    **1 - Using Configuration**
      In module.config.php: top-lever key: service_manager and any of the following sub-key
                  *abastract_factories*
                  *aliases*
                  *factories*
                  *invokables*
                  *services*
                  *shared*
      **2 - Module as Service Providers **
           To provide sevice manager configuration, the Module class must either implement Zend\ModuleManager\Feature\ServiceProviderInterface or the method getServiceConfig().
