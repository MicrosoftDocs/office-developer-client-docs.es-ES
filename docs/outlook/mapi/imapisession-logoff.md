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
ms.openlocfilehash: 317c3702415ddf30038ccd0d40cdf0f19abc61f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338111"
---
# <a name="imapisessionlogoff"></a>IMAPISession::Logoff

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Finaliza una sesión MAPI.
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> a Identificador de la ventana primaria de los cuadros de diálogo o ventanas que se va a mostrar. Este parámetro se omite si no se establece la marca MAPI_LOGOFF_UI.
    
 _ulFlags_
  
> a Máscara de máscara de marcas que controlan la operación de cierre de sesión. Se pueden establecer los siguientes indicadores:
    
MAPI_LOGOFF_SHARED 
  
> Si se comparte esta sesión, todos los clientes que iniciaron sesión con la sesión compartida deben recibir una notificación de la desconexión en curso. Los clientes deben cerrar la sesión. Cualquier cliente que use la sesión compartida puede establecer esta marca. MAPI_LOGOFF_SHARED se omite si la sesión actual no se ha compartido.
    
MAPI_LOGOFF_UI 
  
> **Cierre de sesión** puede mostrar un cuadro de diálogo durante la operación, posiblemente solicitando al usuario que confirme la acción. 
    
 _ulReserved_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de cierre de sesión se realizó correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISession:: Logoff** finaliza una sesión MAPI. Cuando se devuelve el **cierre de sesión** , no se puede llamar a ninguno de los métodos excepto [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando el **cierre** de sesión vuelva, libere el objeto Session mediante una llamada a su método **IUnknown:: Release** . 
  
Para obtener más información acerca de la finalización de una sesión, vea [finalizar una sesión MAPI](ending-a-mapi-session.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIObjects. cpp  <br/> |CMapiObjects:: Logoff  <br/> |MFCMAPI usa el método **IMAPISession:: Logoff** para cerrar la sesión antes de liberarla.  <br/> |
   
> [!NOTE]
> Debido al comportamiento de apagado rápido incluido en Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010 y Microsoft Outlook 2013, los clientes no deben pasar nunca el parámetro **MAPI_LOGOFF_SHARED** a [IMAPISession:: Logoff](imapisession-logoff.md). Si se pasa **MAPI_LOGOFF_SHARED** , todos los clientes MAPI empezarán el apagado y se producirá un comportamiento inesperado. 
  
## <a name="see-also"></a>Vea también



[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Finalizar una sesión MAPI](ending-a-mapi-session.md)

