---
title: Elija una versión específica de MAPI para cargar
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: d0bce7b3a12f259b7ac5f28219c8a92dd2200f07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816967"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a>Elija una versión específica de MAPI para cargar

**Se aplica a**: Outlook 
  
Cuando se vincula explícitamente a una implementación de MAPI, debe seleccionar cuidadosamente qué implementación a cargar. 
  
Existen dos métodos para vincular explícitamente a una implementación de MAPI. 
  
1. Puede cargar la biblioteca de código auxiliar MAPI y especificar en el registro de un archivo DLL personalizado para cargar y distribuir MAPI llamadas a.
    
2. Puede implementar el algoritmo de búsqueda de cliente MAPI para buscar la versión de MAPI utilizado por el cliente de correo predeterminado y lo carga.
    
Debido a que puede cambiar la [Configuración del registro de Mapi32.dll código auxiliar](http://msdn.microsoft.com/en-us/library/ms531218%28EXCHG.10%29.aspx) para dirigir la aplicación para usar cualquier implementación de MAPI, se recomienda que dirigir la aplicación para usar una implementación de MAPI que se han probado con. El siguiente, describe ambos métodos de vinculación de forma explícita. 
  
## <a name="reading-from-the-registry"></a>Lectura del registro

### <a name="to-read-mapi-implementation-information-from-the-registry"></a>Para leer información de implementación de MAPI desde el registro

1. Las claves del registro que indican un archivo DLL personalizado para un cliente de correo se encuentran en la `HKLM\Software\Clients\Mail` clave del cliente de correo. 
    
   En la siguiente tabla se describe estas claves:
    
   |**Clave**|**Descripción**|
   |:-----|:-----|
   |MSIComponentID  <br/> |Llama una categoría de Windows Installer PublishComponent identificador (GUID) que identifica el archivo DLL que se exporta simple MAPI o MAPI. Si esta clave, set tiene prioridad sobre la clave **DLLPath** o **DLLPathEx** .  <br/> |
   |MSIApplicationLCID  <br/> |Identificador de configuración regional (LCID) para la aplicación. La primera cadena de valor identifica una subclave de `HKLM\Software` y valores de cadena subsiguientes identifican los valores del Registro debajo de esta clave que contienen información de configuración regional.  <br/> |
   |MSIOfficeLCID  <br/> |LCID para Microsoft Office. La primera cadena de valor identifica una subclave de `HKLM\Software` y valores de cadena subsiguientes identifican los valores del Registro debajo de esta clave.  <br/> |
   
   Obtener la información de estas claves.
    
2. Pase los valores que obtuvo en el paso anterior a la función [FGetComponentPath](fgetcomponentpath.md) . **FGetComponentPath** es una función que se exporta en la biblioteca de código auxiliar MAPI Mapistub.dll. Devuelve la ruta de acceso de la versión personalizada de MAPI. 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a>Para cargar la implementación de MAPI marcada como predeterminada

1. Leer la `HKLM\Software\Clients\Mail::(default)` valor del registro. 
    
2. Buscar la información para el cliente indicado tal y como se ha descrito anteriormente.
    
> [!NOTE]
> Tenga en cuenta que el cliente de correo predeterminado podría implementar MAPI extendida. 
  
#### <a name="example"></a>Ejemplo

Para cargar MAPI tal como se implementa mediante Outlook, busque las claves del registro bajo `HKLM\Software\Clients\Mail\Microsoft Outlook` y páselos a **FGetComponentPath**. **FGetComponentPath** devolverá la ruta de acceso para la implementación de MAPI de Outlook. 
  
Si no se establecen las claves **MSIComponentID**, **MSIApplicationLCID**y **MSIOfficeLCID** , compruebe el valor de registro **DLLPathEx** . Si se establecen las claves, **FGetComponentPath** proporciona la ruta de acceso de implementación del cliente de MAPI. 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a>Implementar el algoritmo de búsqueda de cliente de MAPI

En la siguiente tabla se enumera las cuatro funciones de MFCMAPI que se usan para buscar la ruta de acceso para una implementación personalizada de MAPI:
  
|**Función**|**Descripción**|
|:-----|:-----|
| `GetMAPIPath` <br/> |Obtiene la ruta de acceso de la biblioteca MAPI.  <br/> |
| `GetMailKey` <br/> |Obtiene la clave del registro de correo MAPI.  <br/> |
| `GetMapiMsiIds` <br/> |Obtiene el identificador de Windows Installer.  <br/> |
| `GetComponentPath` <br/> |Obtiene la ruta de acceso de componente con [FGetComponentPath](fgetcomponentpath.md).  <br/> |
   
Debido a que MFCMAPI carga la implementación predeterminada de MAPI de forma predeterminada, si va a usar una implementación diferente de MAPI, debe dirigir explícitamente que lo haga. Esto se realiza mediante el uso de la rutina de **MAPI Session\Load** . 
  
### <a name="how-these-functions-work"></a>Cómo funcionan estas funciones

1. Las llamadas MFCMAPI `GetMAPIPath`, pasando NULL para el parámetro de cliente, para cargar la implementación de MAPI predeterminada.
    
2.  `GetMAPIPath`las llamadas `GetMapiMsiIds` para leer los valores para **MSIComponentID**, **MSIApplicationLCID**y **MSIOfficeLCID**.
    
3.  `GetMapiMsiIds`las llamadas `GetMailKey` para abrir la clave del registro para el cliente de correo predeterminado. 
    
4.  `GetMapiMsiIds`usa el identificador del registro devuelto por `GetMailKey` para buscar valores de **MSIComponentID**, **MSIApplicationLCID**y **MSIOfficeLCID**.
    
5. Los valores para **MSIComponentID**, **MSIApplicationLCID**y **MSIOfficeLCID**, se devuelven a `GetMAPIPath`.  `GetMAPIPath`a continuación, pasa a `GetComponentPath`.
    
6.  `GetComponentPath`carga la biblioteca de código auxiliar MAPI, Mapi32.dll, desde el directorio del sistema. 
    
7.  `GetComponentPath`a continuación, se recupera la dirección de la función **FGetComponentPath** de Mapi32.dll, suponiendo que Mapi32.dll exporta **FGetComponentPath**.
    
8. Si obtiene la dirección de **FGetComponentPath** de Mapi32.dll se produce un error, `GetComponentPath` recupera la dirección de Mapistub.dll. 
    
9.  `GetComponentPath`a continuación, llama a **FGetComponentPath**, obtener la ruta de acceso de la versión predeterminada de MAPI.
    
10.  `GetMAPIPath`a continuación, devuelve esta ruta de acceso para el autor de la llamada, que, a continuación, carga MAPI y se vincula explícitamente a él tal como se describe en el [vínculo a las funciones de MAPI](how-to-link-to-mapi-functions.md).
    
> [!NOTE] 
> - Para admitir copias localizados de MAPI para inglés y configuraciones regionales que no sean inglés, `GetMAPIPath` lee los valores de las subclaves de **MSIApplicationLCID** y **MSIOfficeLCID** .  `GetMAPIPath`a continuación, llama a **FGetComponentPath**, especificando primero **MSIApplicationLCID** como **szQualifier**y vuelva a especificar **MSIOfficeLCID** como **szQualifier**. Para obtener más información acerca de las claves del registro para los clientes de correo que admiten idiomas distintos del inglés, consulte [Configuración de las teclas de MSI para una DLL de MAPI](http://msdn.microsoft.com/en-us/library/ee909494%28VS.85%29.aspx).   
> - Si MFCMAPI no recibe una ruta de acceso para el uso de MAPI `GetMAPIPath`, que carga la biblioteca de código auxiliar MAPI desde el directorio del sistema.
> - El valor de registro **MSMapiApps** tratado en [Explícitamente asignación de las llamadas MAPI a los archivos DLL de MAPI](http://msdn.microsoft.com/en-us/library/ee909490%28VS.85%29.aspx) sólo se aplica cuando se usa la biblioteca de código auxiliar de MAPI. Las aplicaciones que carga una implementación específica de MAPI o de carga de la implementación predeterminada no es necesario establecer la clave del registro **MSMapiApps** . 
    
## <a name="see-also"></a>Ver también

- [FGetComponentPath](fgetcomponentpath.md)
- [Informaci�n general sobre programaci�n de MAPI](mapi-programming-overview.md)
- [Vínculo a funciones de MAPI](how-to-link-to-mapi-functions.md)
- [Configuración de Mapi32.dll código auxiliar del registro](http://msdn.microsoft.com/en-us/library/ms531218%28EXCHG.10%29.aspx)
- [Configuración de las claves MSI para el archivo DLL de MAPI](http://msdn.microsoft.com/en-us/library/ee909494%28VS.85%29.aspx)
- [Asignación explícitamente las llamadas MAPI a los archivos DLL MAPI](http://msdn.microsoft.com/en-us/library/ee909490%28VS.85%29.aspx)

