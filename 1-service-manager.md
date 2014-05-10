
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


**Service Manager Configuration**
    *1 - Using Configuration*
      In module.config.php: top-lever key: service_manager and any of the following sub-key
                  *abastract_factories*
                  *aliases*
                  *factories*
                  *invokables*
                  *services*
                  *shared*
      *2 - Module as Service Providers *
           To provide sevice manager configuration, the Module class must either implement Zend\ModuleManager\Feature\ServiceProviderInterface or the method getServiceConfig().
