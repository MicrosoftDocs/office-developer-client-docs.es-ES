---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: Realiza la categorización de envío posterior a la en un elemento de correo en función de su PidTagConversationId.
ms.openlocfilehash: efecfc2d0d865428cb958fc15a858bbc7807c5d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816085"
---
# <a name="hrprocessconvactionforsentitem"></a>HrProcessConvActionForSentItem

Realiza la categorización de envío posterior a la en un elemento de correo en función de su [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Exportada por:  <br/> |Outlook.exe  <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Se implementa mediante:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a>Parámetros

_pmbinStoreEid_
  
> [entrada] [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) de la tienda o el [PidTagStoreEntryId](http://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) del elemento de correo. No puede ser NULL o no es válido. 
    
_pmbinMsgEid_
  
> [entrada] [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) del elemento de correo. No puede ser NULL o no es válido. 
    
_pmbinConvID_
  
> [entrada] [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) del elemento de correo. No puede ser NULL o no es válido. 
    
_dwFlags_
  
> [entrada] Una máscara de bits que especifica información adicional acerca de la llamada al método.
    
   - 0: no hay opciones adicionales que se usan en esta llamada al método. Éste es el valor recomendado. 
    
   - **PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ es realmente el [PidTagSearchKey](http://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) del mensaje. Uso de un **PidTagSearchKey** es muchos recursos y se debe evitar si está disponible un [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) . 
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada tuvo éxito.  <br/> |
|E_INVALIDARG  <br/> | _dwFlags_ contiene un indicador desconocido.  <br/> |
   
## <a name="remarks"></a>Comentarios

Las categorías se consideran información personal y no deberían ser transmitidas fuera del buzón del usuario. Por lo tanto, no llame a **HrProcessConvActionForSentItem** en un elemento de correo no enviados. En su lugar, enviar el elemento y, a continuación, llamar a **HrProcessConvActionForSentItem** en la copia archivada. La copia archivada puede almacenarse en la carpeta Elementos enviados, o en una ubicación equivalente. 
  
La aplicación debe ser en proceso con Outlook.exe, por ejemplo, desde un complemento COM, llamar a **HrProcessConvActionForSentItem**. Si intenta llamar a **HrProcessConvActionForSentItem** fuera de proceso, **HrProcessConvActionForSentItem** producirá una excepción de infracción de acceso. 
  

