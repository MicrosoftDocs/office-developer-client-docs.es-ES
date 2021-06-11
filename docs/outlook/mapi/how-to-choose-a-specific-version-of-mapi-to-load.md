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
  
Al vincular explícitamente a una implementación de MAPI, debe seleccionar cuidadosamente qué implementación cargar. 
  
Hay dos métodos para vincular explícitamente a una implementación de MAPI. 
  
1. Puede cargar la biblioteca de código auxiliar MAPI y especificar en el Registro una DLL personalizada a la que cargar y enviar llamadas MAPI.
    
2. Puede implementar el algoritmo de búsqueda de cliente MAPI para buscar la versión de MAPI usada por el cliente de correo predeterminado y cargarla.
    
Dado que puede [](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) cambiar elMapi32.dll registro de código auxiliar Configuración para que la aplicación use cualquier implementación de MAPI, le recomendamos que dirija a la aplicación a usar una implementación de MAPI con la que haya probado. A continuación se describen ambos métodos de vinculación explícitamente. 
  
## <a name="reading-from-the-registry"></a>Lectura desde el Registro

### <a name="to-read-mapi-implementation-information-from-the-registry"></a>Para leer la información de implementación mapi desde el Registro

1. Las claves del Registro que indican una DLL personalizada para un cliente de correo se encuentran bajo  `HKLM\Software\Clients\Mail` la clave del cliente de correo. 
    
   En la tabla siguiente se describen estas claves:
    
   |**Tecla**|**Descripción**|
   |:-----|:-----|
   |MSIComponentID  <br/> |Un Windows de categoría PublishComponent (GUID) del instalador que identifica el DLL que exporta llamadas MAPI o MAPI sencillas. Si se establece, esta clave tiene prioridad sobre **la clave DLLPath** o **DLLPathEx.**  <br/> |
   |MSIApplicationLCID  <br/> |Identificador de configuración regional (LCID) para la aplicación. El primer valor de cadena identifica una subclave desde y los valores de cadena subsiguientes identifican los valores del Registro debajo de  `HKLM\Software` esta clave que contienen información de configuración regional.  <br/> |
   |MSIOfficeLCID  <br/> |LCID para Microsoft Office. El primer valor de cadena identifica una subclave desde y los valores de cadena subsiguientes identifican los valores  `HKLM\Software` del Registro debajo de esta clave.  <br/> |
   
   Obtenga la información de estas claves.
    
2. Pase los valores obtenidos del paso anterior a la [función FGetComponentPath.](fgetcomponentpath.md) **FGetComponentPath es** una función exportada por la biblioteca de códigos auxiliares MAPI Mapistub.dll. Devuelve la ruta de acceso de la versión personalizada de MAPI. 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a>Para cargar la implementación de MAPI marcada como predeterminada

1. Lea el  `HKLM\Software\Clients\Mail::(default)` valor del Registro. 
    
2. Busque la información del cliente indicado como se describió anteriormente.
    
> [!NOTE]
> Tenga en cuenta que es posible que el cliente de correo predeterminado no implemente MAPI extendido. 
  
#### <a name="example"></a>Ejemplo

Para cargar MAPI según lo implementado por Outlook, busque las claves del Registro en y pásenlas `HKLM\Software\Clients\Mail\Microsoft Outlook` a **FGetComponentPath**. **FGetComponentPath** devolverá la ruta de acceso para Outlook implementación de MAPI. 
  
Si las claves **MSIComponentID,** **MSIApplicationLCID** y **MSIOfficeLCID** no están establecidas, compruebe el valor del Registro **DLLPathEx.** Si se establecen las claves, **FGetComponentPath** proporciona la ruta de acceso de la implementación del cliente de MAPI. 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a>Implementación del algoritmo de búsqueda de cliente MAPI

En la tabla siguiente se enumeran las cuatro funciones de MFCMAPI que se usan para buscar la ruta de acceso de una implementación personalizada de MAPI:
  
|**Función**|**Descripción**|
|:-----|:-----|
| `GetMAPIPath` <br/> |Obtiene la ruta de acceso de la biblioteca MAPI.  <br/> |
| `GetMailKey` <br/> |Obtiene la clave del Registro de correo MAPI.  <br/> |
| `GetMapiMsiIds` <br/> |Obtiene el identificador Windows installer.  <br/> |
| `GetComponentPath` <br/> |Obtiene la ruta de acceso del componente [mediante FGetComponentPath](fgetcomponentpath.md).  <br/> |
   
Dado que MFCMAPI carga la implementación predeterminada de MAPI de forma predeterminada, si desea usar una implementación diferente de MAPI, debe dirigirla explícitamente para hacerlo. Esto se realiza mediante la **rutina Session\Load MAPI.** 
  
### <a name="how-these-functions-work"></a>Cómo funcionan estas funciones

1. MFCMAPI llama  `GetMAPIPath` , pasando NULL para el parámetro de cliente, para cargar la implementación MAPI predeterminada.
    
2.  `GetMAPIPath` llamadas  `GetMapiMsiIds` para leer los valores de **MSIComponentID,** **MSIApplicationLCID** y **MSIOfficeLCID**.
    
3.  `GetMapiMsiIds` llamadas  `GetMailKey` para abrir la clave del Registro para el cliente de correo predeterminado. 
    
4.  `GetMapiMsiIds` usa el controlador del Registro devuelto por para buscar valores  `GetMailKey` para **MSIComponentID,** **MSIApplicationLCID** y **MSIOfficeLCID**.
    
5. Los valores de **MSIComponentID,** **MSIApplicationLCID** y **MSIOfficeLCID**, se devuelven a  `GetMAPIPath` .  `GetMAPIPath` a continuación, los pasa a  `GetComponentPath` .
    
6.  `GetComponentPath` carga la biblioteca de código auxiliar MAPI, Mapi32.dll, desde el directorio del sistema. 
    
7.  `GetComponentPath` a continuación, recupera la dirección de la función **FGetComponentPath** desde Mapi32.dll, suponiendo que Mapi32.dll exporta **FGetComponentPath**.
    
8. Si se produce un error al obtener la dirección de **FGetComponentPath** Mapi32.dll, recupera  `GetComponentPath` la dirección de Mapistub.dll. 
    
9.  `GetComponentPath` a continuación, **llama a FGetComponentPath**, obteniendo la ruta de acceso de la versión predeterminada de MAPI.
    
10.  `GetMAPIPath` a continuación, devuelve esta ruta de acceso al autor de la llamada, que luego carga MAPI y se vincula explícitamente a ella como se describe [en Vínculo a funciones MAPI](how-to-link-to-mapi-functions.md).
    
> [!NOTE] 
> - Para admitir copias localizadas de MAPI para configuraciones regionales en inglés y no inglesas, lee los valores de las `GetMAPIPath` subclaves **MSIApplicationLCID** y **MSIOfficeLCID.**  `GetMAPIPath` a continuación, llama **a FGetComponentPath**, primero especifica **MSIApplicationLCID** como **szQualifier** y, de nuevo, especifica **MSIOfficeLCID** **como szQualifier**. Para obtener más información acerca de las claves del Registro para clientes de correo que admiten idiomas que no son inglés, vea [Setting Up the MSI Keys for Your MAPI DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).   
> - Si MFCMAPI no recibe una ruta de acceso para MAPI mediante , carga la biblioteca de código  `GetMAPIPath` auxiliar MAPI desde el directorio del sistema.
> - El valor del Registro **MSMapiApps** que se describe en [Asignación](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) explícita de llamadas MAPI a DLL MAPI solo se aplica cuando se usa la biblioteca auxiliar MAPI. Las aplicaciones que cargan una implementación específica de MAPI o cargan la implementación predeterminada no tienen que establecer la clave del Registro **MSMapiApps.** 
    
## <a name="see-also"></a>Vea también

- [FGetComponentPath](fgetcomponentpath.md)
- [Información general sobre programación de MAPI](mapi-programming-overview.md)
- [Vínculo a funciones MAPI](how-to-link-to-mapi-functions.md)
- [Mapi32.dll registro de código auxiliar Configuración](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [Configuración de las claves MSI para su DLL MAPI](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [Asignación explícita de llamadas MAPI a DLL MAPI](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

