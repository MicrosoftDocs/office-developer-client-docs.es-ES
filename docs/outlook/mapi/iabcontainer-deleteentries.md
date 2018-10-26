---
title: IABContainerDeleteEntries
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.DeleteEntries
api_type:
- COM
ms.assetid: 70a24811-0c41-4b44-8c63-7ef807bc9051
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4140dc39b7f866b0372e5940aef5efc0524ad593
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573113"
---
# <a name="iabcontainerdeleteentries"></a>IABContainer::DeleteEntries

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Quita una o más entradas, normalmente otros contenedores, listas de distribución o a los usuarios de mensajería.
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpEntries_
  
> [entrada] Un puntero a una matriz de estructuras [ENTRYLIST](entrylist.md) que contienen los identificadores de entrada que representan las entradas que se va a eliminar. 
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las entradas especificadas se han eliminado correctamente. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se ha realizado correctamente, pero no se podrían eliminar uno o más de las entradas. Cuando se devuelve este valor, la llamada se debe controlarse como correcta. Para probar este valor, utilice la macro **HR_FAILED** . Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|Abdlg.cpp  <br/> |CabDlg::OnDeleteSelectedItem  <br/> |MFCMAPI usa el método **DeleteEntries** para eliminar una entrada específica de un contenedor de la libreta de direcciones.  <br/> |
   
## <a name="see-also"></a>Vea también



[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

