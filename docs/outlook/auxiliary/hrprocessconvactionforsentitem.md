---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: Realiza la categorización posterior al envío en un elemento de correo basado en su PidTagConversationId.
ms.openlocfilehash: 675f308093eea30084271abc66c1fa66e2ad6828
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318903"
---
# <a name="hrprocessconvactionforsentitem"></a>HrProcessConvActionForSentItem

Realiza la categorización posterior al envío en un elemento de correo basado en [su PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Exportado por:  <br/> |Outlook.exe  <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a>Parámetros

_pmbinStoreEid_
  
> [entrada] [PidTagEntryId del](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) almacén o [PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) del elemento de correo. No puede ser NULL o no válido. 
    
_pmbinMsgEid_
  
> [entrada] [PidTagEntryId del](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) elemento de correo. No puede ser NULL o no válido. 
    
_pmbinConvID_
  
> [entrada] [PidTagConversationId del](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) elemento de correo. No puede ser NULL o no válido. 
    
_dwFlags_
  
> [entrada] Máscara de bits que especifica información adicional sobre la llamada al método.
    
   - 0: no se usan opciones adicionales en esta llamada de método. Este es el valor recomendado. 
    
   - **PCAFSIF_MSGEID_IS_SEARCH_KEY:** _pmbinMsgEid_ es en realidad [pidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) del mensaje. El uso **de PidTagSearchKey** consume muchos recursos y debe evitarse si un [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) está disponible. 
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada se ha realizado correctamente.  <br/> |
|E_INVALIDARG  <br/> | _dwFlags_ contiene una marca desconocida.  <br/> |
   
## <a name="remarks"></a>Comentarios

Las categorías se consideran información personal y no deben transmitirse fuera del buzón del usuario. Por lo tanto, no llame **a HrProcessConvActionForSentItem** en un elemento de correo no enviado. En su lugar, envíe el elemento y, a continuación, llame a **HrProcessConvActionForSentItem** en la copia archivada. La copia archivada puede almacenarse en la carpeta Elementos enviados o en una ubicación equivalente. 
  
La aplicación debe estar en proceso con Outlook.exe, como desde un complemento COM, para llamar a **HrProcessConvActionForSentItem**. Si intenta llamar a **HrProcessConvActionForSentItem** fuera de proceso, **HrProcessConvActionForSentItem** producirá una excepción de infracción de acceso. 
  

