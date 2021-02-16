---
title: HrGetAutoDiscoverXML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetAutoDiscoverXML
api_type:
- COM
ms.assetid: 03691187-7c65-620b-576f-6ebe62a80830
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 77f28654ffe0f6f459fde229bb7428f2c39e96c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347806"
---
# <a name="hrgetautodiscoverxml"></a>HrGetAutoDiscoverXML

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una secuencia de lenguaje de marcado extensible (XML) que representa la información recuperada del servicio de detección automática de un servidor de Microsoft Exchange 2007.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Exportado por:  <br/> |olmapi32.dll  <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a>Parámetros

 _pwzAddress_
  
> [entrada] Una dirección de correo electrónico smtp (Protocolo simple de transferencia de correo) terminada en null de la cuenta para la que desea recuperar la información de detección automática.
    
 _pwzPassword_
  
> [entrada] Una contraseña opcional para la cuenta especificada por  _pwzAddress_. Tenga en cuenta que pasar cualquier contraseña no tiene ningún efecto si la cuenta especificada por  _pwzAddress_ no requiere una contraseña. 
    
 _hCancelEvent_
  
> [entrada] Un identificador de evento win32 sin establecer que es opcional y se puede usar para cancelar la operación. Para cancelar la operación, establezca el evento y pase el identificador de evento  _como hCancelEvent_; pass **null** si no desea cancelar la operación. Tenga en cuenta que pasar un valor que no representa un identificador de evento no tiene ningún efecto y la función lo omite. 
    
 _ulFlags_
  
> [entrada] Este parámetro no se usa. Debe ser 0.
    
 _ppXmlStream_
  
> [salida] Puntero a un [objeto IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) que contiene el XML de detección automática. Devuelve **null** si se produce un error en la operación de detección automática. Debes liberar el [objeto IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) cuando termines con él. 
    
## <a name="return-values"></a>Valores devueltos

S_OK 
  
- La llamada a la función se realiza correctamente.
    
E_INVALIDARG 
  
-  _pwzAddress_ es **null** o no es una dirección SMTP válida, o _ppXmlStream_ es un puntero nulo **a** un objeto [IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) 
    
MAPI_E_NOT_FOUND 
  
- El equipo cliente no está conectado a la red, el equipo cliente no está conectado a un servidor de Microsoft Exchange 2007,  _pwzAddress_ no es una cuenta en un servidor de Exchange 2007 o  _pwzAddress_ es una cuenta que no admite el servicio de detección automática de Exchange. 
    
MAPI_E_USER_CANCEL 
  
- Se ha pasado un identificador de evento  _a hCancelEvent_ para cancelar la operación. 
    
STRSAFE_E_INSUFFICIENT_BUFFER
  
- El valor pasado  _a pwzAddress_ o  _pwzPassword_ es demasiado largo, por lo que desborda el búfer interno de tamaño de 256 bytes. 
    

