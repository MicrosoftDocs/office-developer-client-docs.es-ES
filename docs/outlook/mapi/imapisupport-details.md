---
title: IMAPISupportDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Details
api_type:
- COM
ms.assetid: 1a62efa2-dd6b-4acb-a760-defa601c20c9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9923813d821e2b34497e3b498c19ce22ceda2eb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817482"
---
# <a name="imapisupportdetails"></a>IMAPISupport::Details

  
  
**Hace referencia a**: Outlook 
  
Muestra un cuadro de diálogo que muestra detalles acerca de una entrada de la libreta de direcciones determinada.
  
```cpp
HRESULT Details(
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpulUIParam_
  
> [out] Un puntero al identificador de la ventana principal del cuadro de diálogo devuelto.
    
 _lpfnDismiss_
  
> [entrada] Un puntero a una función basándose en el prototipo [DISMISSMODELESS](dismissmodeless.md) o NULL. Este miembro sólo se aplica a la versión del cuadro de diálogo no modal indicada por el indicador DIALOG_SDI que se va a establecer. MAPI llama a la función **DISMISSMODELESS** cuando el usuario cierra el cuadro de diálogo no modal de dirección, que le informa de un cliente que llama a **IMAPISupport::Details** que el cuadro de diálogo ya no está activo. 
    
 _lpvDismissContext_
  
> [entrada] Un puntero a la información de contexto para pasar a la función **DISMISSMODELESS** indicada por el parámetro _lpfnDismiss_ . Este parámetro sólo se aplica a la versión del cuadro de diálogo no modal mediante la inclusión de la marca DIALOG_SDI en el parámetro _ulFlags indicado_ . 
    
 _cbEntryID_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada para la que se muestran los detalles.
    
 _lpfButtonCallback_
  
> [entrada] Un puntero a una función según el prototipo de función [LPFNBUTTON](lpfnbutton.md) . Una función **LPFNBUTTON** agrega un botón en el cuadro de diálogo detalles. 
    
 _lpvButtonContext_
  
> [entrada] Un puntero a datos que se usa como un parámetro para la función especificada por el parámetro _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> [entrada] Un puntero a una cadena que contiene el texto que se aplicará a la se ha agregado un botón si ese botón es extensible. El parámetro _lpszButtonText_ debe ser NULL si no se necesita un botón extensible. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el tipo de texto para el parámetro _lpszButtonText_ . Se puede establecer la marca siguiente: 
    
DIALOG_MODAL
  
> Mostrar la versión modal del cuadro de diálogo dirección comunes. Este marcador es mutuamente excluyente con DIALOG_SDI.
    
DIALOG_SDI
  
>  Mostrar la versión del cuadro de diálogo dirección comunes no modal. Este marcador es mutuamente excluyente con DIALOG_MODAL. 
    
MAPI_UNICODE. 
  
> Las cadenas que se pasan en están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El cuadro de diálogo detalles se mostró correctamente para la entrada de la libreta de direcciones.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::Details** se implementa para objetos de compatibilidad con de proveedor de la libreta de direcciones. Los proveedores de la libreta de direcciones, llame a **Detalles** para mostrar un cuadro de diálogo que proporciona detalles sobre una entrada determinada en la libreta de direcciones. Los parámetros _lpfButtonCallback_, _lpvButtonContext_y _lpszButtonText_ se pueden usar para agregar un botón definido por el cliente para el cuadro de diálogo. Cuando se hace clic en el botón, MAPI llama a la función de devolución de llamada que apunta _lpfButtonCallback_, pasando el identificador de entrada de los datos y el botón en _lpvButtonContext_. Si no es necesario un botón extensible, _lpszButtonText_ debe ser nulo. 
  
## <a name="see-also"></a>Vea también



[ADRPARM](adrparm.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

