---
title: IMAPISessionLogoff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Logoff
api_type:
- COM
ms.assetid: 93e38f6c-4b67-4f2d-bc94-631efec86852
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7d6ccd64fea0af30e81a2db0bcb9630062b4b64d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817436"
---
# <a name="imapisessionlogoff"></a>IMAPISession::Logoff

  
  
**Hace referencia a**: Outlook 
  
Termina una sesión MAPI.
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a>Parámetros

 _ulUIParam_
  
> [entrada] Identificador de la ventana principal de los cuadros de diálogo o windows que se mostrará. Este parámetro se omite si no se establece la marca MAPI_LOGOFF_UI.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controlan la operación de cierre de sesión. Se pueden establecer los siguientes indicadores:
    
MAPI_LOGOFF_SHARED 
  
> Si se comparte esta sesión, todos los clientes que inició la sesión mediante el uso de la sesión compartida se le deben notificar el cierre de sesión en curso. Deben cerrar la sesión de los clientes. Cualquier cliente que está usando la sesión compartida puede establecer esta marca. MAPI_LOGOFF_SHARED se omite si no se comparte la sesión actual.
    
MAPI_LOGOFF_UI 
  
> **Cierre de sesión** puede mostrar un cuadro de diálogo durante la operación, posiblemente pedir confirmación al usuario. 
    
 _ulReserved_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de cierre de sesión fue correcta.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISession::Logoff** finaliza una sesión MAPI. Cuando se devuelve el **cierre de sesión** , se puede llamar a ninguno de los métodos excepto [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando se devuelve el **cierre de sesión** , liberar el objeto de sesión llamando a su método **IUnknown:: Release** . 
  
Para obtener más información acerca de terminar una sesión, vea [Finalizar una sesión de MAPI](ending-a-mapi-session.md).
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::Logoff  <br/> |MFCMAPI usa el método **IMAPISession::Logoff** para cerrar la sesión antes de enviarlo.  <br/> |
   
> [!NOTE]
> Debido al comportamiento de apagado rápido que se introdujo en Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010 y Microsoft Outlook 2013, los clientes nunca deben pasar el parámetro **MAPI_LOGOFF_SHARED** a [IMAPISession::Logoff](imapisession-logoff.md). Pasando **MAPI_LOGOFF_SHARED** hará que todos los clientes MAPI empezar el cierre y se producirá un comportamiento inesperado. 
  
## <a name="see-also"></a>Vea también



[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)
  
[Finalizar una sesión MAPI](ending-a-mapi-session.md)

