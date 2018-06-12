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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: da466fc9add8cbc385014782f31749d3b6522da9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817043"
---
# <a name="hrgetautodiscoverxml"></a>HrGetAutoDiscoverXML

  
  
**Se aplica a**: Outlook 
  
Devuelve una secuencia de lenguaje de marcado Extensible (XML) que representa información recuperada desde el servicio de detección automática de un servidor de Microsoft Exchange 2007.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Exportada por:  <br/> |olmapi32.dll  <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Se implementa mediante:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a>Sintaxis

 _pwzAddress_
  
> [entrada] Una terminada en null Protocolo Simple de transferencia de correo (SMTP) dirección de correo electrónico de la cuenta para la que desea recuperar la información de detección automática.
    
 _pwzPassword_
  
> [entrada] Una contraseña opcional para la cuenta especificada por _pwzAddress_. Tenga en cuenta que pasar cualquier contraseña no tiene ningún efecto si la cuenta especificada por _pwzAddress_ no requiere una contraseña. 
    
 _hCancelEvent_
  
> [entrada] Un identificador de evento de Win32 no establecido al que es opcional y se puede usar para cancelar la operación. Para cancelar la operación, establezca el evento y pase el identificador de evento como _hCancelEvent_; pase **null** si no desea cancelar la operación. Tenga en cuenta que si se pasa un valor que no representa un identificador de evento no tiene ningún efecto y se omite por la función. 
    
 _ulFlags_
  
> [entrada] Este parámetro no se usa. Debe ser 0.
    
 _ppXmlStream_
  
> [out] Un puntero a un objeto [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) que contiene el XML de detección automática. Devuelve **null** si se produce un error en la operación de detección automática. Debe liberar el objeto [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) cuando haya terminado con él. 
    
## <a name="return-values"></a>Valores devueltos

S_OK 
  
- La llamada a la función es correcta.
    
E_INVALIDARG 
  
-  _pwzAddress_ es **null** o no es una dirección SMTP válida, o _ppXmlStream_ es un puntero **nulo** a un objeto [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) . 
    
MAPI_E_NOT_FOUND 
  
- Equipo cliente no está conectado a la red, equipo cliente no está conectado a un servidor de Microsoft Exchange 2007, _pwzAddress_ no es una cuenta en un servidor de Exchange 2007 o _pwzAddress_ es una cuenta que no es compatible con Exchange servicio de detección automática. 
    
MAPI_E_USER_CANCEL 
  
- Se ha pasado un identificador de evento a _hCancelEvent_ para cancelar la operación. 
    
STRSAFE_E_INSUFFICIENT_BUFFER
  
- El valor pasado a _pwzAddress_ o _pwzPassword_ es demasiado largo, por ejemplo, que desborda el búfer interno de tamaño de 256 bytes. 
    

