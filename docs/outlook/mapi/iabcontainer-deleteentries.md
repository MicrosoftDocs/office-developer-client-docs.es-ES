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
ms.openlocfilehash: e3b238129e55e03da33ef3af75ecce7e73fbad03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425599"
---
# <a name="iabcontainerdeleteentries"></a>IABContainer::DeleteEntries

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Quita una o más entradas, normalmente usuarios de mensajería, listas de distribución u otros contenedores.
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpEntries_
  
> [in] Puntero a una matriz de [estructuras ENTRYLIST](entrylist.md) que contienen identificadores de entrada que representan las entradas que se eliminan. 
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las entradas especificadas se han eliminado correctamente. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se ha hecho correctamente, pero no se pudo eliminar una o varias de las entradas. Cuando se devuelve este valor, la llamada debe controlarse como correcta. Para probar este valor, use la **HR_FAILED** macro. Para obtener más información, vea [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|Abdlg.cpp  <br/> |CabDlg::OnDeleteSelectedItem  <br/> |MFCMAPI usa el **método DeleteEntries** para eliminar una entrada específica de un contenedor de libreta de direcciones.  <br/> |
   
## <a name="see-also"></a>Vea también



[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

