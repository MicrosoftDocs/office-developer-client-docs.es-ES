---
title: Elegir una versión específica de MAPI para cargar
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d353eba55e33b8ab48b3c47d2f31f1b5e0973b58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344523"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a>Elegir una versión específica de MAPI para cargar

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Al vincular explícitamente a una implementación de MAPI, debe seleccionar cuidadosamente la implementación que se va a cargar. 
  
Hay dos métodos que se vinculan explícitamente a una implementación de MAPI. 
  
1. Puede cargar la biblioteca de código auxiliar MAPI y especificar en el registro una DLL personalizada para cargar y enviar llamadas MAPI.
    
2. Puede implementar el algoritmo de búsqueda de cliente MAPI para buscar la versión de MAPI usada por el cliente de correo predeterminado y cargarla.
    
Debido a que puede cambiar la [configuración del registro de código auxiliar Mapi32. dll](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) para dirigir la aplicación para que use cualquier implementación de MAPI, le recomendamos que dirija la aplicación para que use una implementación de MAPI que haya probado con. A continuación, se describen ambos métodos de vinculación explícitamente. 
  
## <a name="reading-from-the-registry"></a>Lectura del registro

### <a name="to-read-mapi-implementation-information-from-the-registry"></a>Para leer la información de implementación de MAPI desde el registro

1. Las claves del registro que indican que un archivo DLL personalizado para un cliente de correo `HKLM\Software\Clients\Mail` se encuentran bajo la clave del cliente de correo. 
    
   En la tabla siguiente se describen estas claves:
    
   |**Tecla**|**Descripción**|
   |:-----|:-----|
   |MSIComponentID  <br/> |Un identificador de categoría (GUID) de PublishComponent de Windows Installer que identifica el archivo DLL que exporta llamadas MAPI simples o MAPI. Si se establece, esta clave tiene prioridad sobre la clave **DLLPath** o **DLLPathEx** .  <br/> |
   |MSIApplicationLCID  <br/> |Identificador de configuración regional (LCID) de la aplicación. El primer valor de cadena identifica una subclave desde `HKLM\Software` y los valores de cadena posteriores identifican valores del registro debajo de esta clave que contienen información de la configuración regional.  <br/> |
   |MSIOfficeLCID  <br/> |LCID para Microsoft Office. El primer valor de cadena identifica una subclave desde `HKLM\Software` y los valores de cadena posteriores identifican valores del registro debajo de esta clave.  <br/> |
   
   Obtenga la información de estas claves.
    
2. Pase los valores que obtuvo del paso anterior a la función [FGetComponentPath](fgetcomponentpath.md) . **FGetComponentPath** es una función que exporta la biblioteca de código auxiliar de MAPI MAPISTUB. dll. Devuelve la ruta de acceso de la versión personalizada de MAPI. 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a>Para cargar la implementación de MAPI marcada como predeterminada

1. Lea el `HKLM\Software\Clients\Mail::(default)` valor del registro. 
    
2. Busque la información para el cliente indicado como se describió anteriormente.
    
> [!NOTE]
> Tenga en cuenta que es posible que el cliente de correo predeterminado no implemente MAPI extendida. 
  
#### <a name="example"></a>Ejemplo

Para cargar MAPI tal y como lo ha implementado Outlook, busque las `HKLM\Software\Clients\Mail\Microsoft Outlook` claves del registro en y pásela a **FGetComponentPath**. **FGetComponentPath** devolverá la ruta de acceso para la implementación de MAPI de Outlook. 
  
Si no se establecen las claves **MSIComponentID**, **MSIApplicationLCID**y **MSIOfficeLCID** , compruebe el valor del registro **DLLPathEx** . Si se establecen las claves, **FGetComponentPath** proporciona la ruta de la implementación del cliente de MAPI. 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a>Implementación del algoritmo de búsqueda del cliente MAPI

En la siguiente tabla se enumeran las cuatro funciones de MFCMAPI que se usan para buscar la ruta de acceso para una implementación personalizada de MAPI:
  
|**Función**|**Descripción**|
|:-----|:-----|
| `GetMAPIPath` <br/> |Obtiene la ruta de acceso de la biblioteca MAPI.  <br/> |
| `GetMailKey` <br/> |Obtiene la clave del registro de correo de MAPI.  <br/> |
| `GetMapiMsiIds` <br/> |Obtiene el identificador de Windows Installer.  <br/> |
| `GetComponentPath` <br/> |Obtiene la ruta de acceso del componente mediante [FGetComponentPath](fgetcomponentpath.md).  <br/> |
   
Debido a que MFCMAPI carga la implementación predeterminada de MAPI de forma predeterminada, si desea usar una implementación diferente de MAPI, debe dirigirla explícitamente para que lo haga. Esto se realiza mediante la rutina **MAPI Session\Load** . 
  
### <a name="how-these-functions-work"></a>Funcionamiento de estas funciones

1. Llamadas `GetMAPIPath`MFCMAPI, pasando null para el parámetro Client, para cargar la implementación MAPI predeterminada.
    
2.  `GetMAPIPath`llamadas `GetMapiMsiIds` para leer los valores de **MSIComponentID**, **MSIApplicationLCID**y **MSIOfficeLCID**.
    
3.  `GetMapiMsiIds`llamadas `GetMailKey` para abrir la clave del registro para el cliente de correo predeterminado. 
    
4.  `GetMapiMsiIds`usa el controlador del registro devuelto `GetMailKey` por para buscar valores para **MSIComponentID**, **MSIApplicationLCID**y **MSIOfficeLCID**.
    
5. Los valores de **MSIComponentID**, **MSIApplicationLCID**y **MSIOfficeLCID**se devuelven a `GetMAPIPath`.  `GetMAPIPath`a continuación, los `GetComponentPath`pasa a.
    
6.  `GetComponentPath`carga la biblioteca de código auxiliar MAPI, Mapi32. dll, del directorio del sistema. 
    
7.  `GetComponentPath`a continuación, recupera la dirección de la función **FGetComponentPath** de Mapi32. dll, suponiendo que Mapi32. dll exporte **FGetComponentPath**.
    
8. Si se produce un error al obtener la dirección de **FGetComponentPath** de `GetComponentPath` Mapi32. dll, recupera la dirección de MAPISTUB. dll. 
    
9.  `GetComponentPath`a continuación, llama a **FGetComponentPath**, para obtener la ruta de acceso de la versión predeterminada de MAPI.
    
10.  `GetMAPIPath`a continuación, devuelve esta ruta de acceso al autor de la llamada, que, a continuación, carga MAPI y se vincula explícitamente, tal como se describe en [Link to MAPI Functions](how-to-link-to-mapi-functions.md).
    
> [!NOTE] 
> - Para admitir copias localizadas de MAPI para las configuraciones regionales en inglés y en otros `GetMAPIPath` idiomas, lea los valores de las subclaves **MSIApplicationLCID** y **MSIOfficeLCID** .  `GetMAPIPath`a continuación, llama a **FGetComponentPath**, especifica primero **MSIApplicationLCID** como **szQualifier**y, de nuevo, especifica **MSIOfficeLCID** como **szQualifier**. Para obtener más información acerca de las claves del registro para los clientes de correo que admiten idiomas distintos del inglés, consulte Configuring [The MSI Keys for your MAPI dll](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).   
> - Si MFCMAPI no recibe una ruta de acceso para MAPI `GetMAPIPath`con, carga la biblioteca de código auxiliar MAPI desde el directorio del sistema.
> - El valor del registro **MSMapiApps** que se describe en [asignación explícita de llamadas MAPI a dll MAPI](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) solo se aplica cuando se utiliza la biblioteca de código auxiliar de MAPI. Las aplicaciones que cargan una implementación específica de MAPI o cargan la implementación predeterminada no tienen que establecer la clave del registro **MSMapiApps** . 
    
## <a name="see-also"></a>Vea también

- [FGetComponentPath](fgetcomponentpath.md)
- [Información general sobre programación de MAPI](mapi-programming-overview.md)
- [Vínculo a funciones MAPI](how-to-link-to-mapi-functions.md)
- [Configuración del registro de código auxiliar de Mapi32. dll](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [Configuración de las claves MSI para la DLL de MAPI](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [Asignación explícita de llamadas MAPI a dll MAPI](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

