---
title: HrDecomposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeEID
api_type:
- COM
ms.assetid: 4847838a-2ad8-4927-8f78-7fa5c8eb54eb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7cae156e29503c8b50755c99023805aa6d14e704
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573372"
---
# <a name="hrdecomposeeid"></a>HrDecomposeEID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Separa el identificador de entrada compuesta de un objeto, normalmente un mensaje en un almacén de mensajes, en el identificador de entrada de ese objeto en el almacén y el identificador de entrada de la tienda.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
HrDecomposeEID(
  LPMAPISESSION psession,
  ULONG cbEID,
  LPENTRYID pEID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a>Parámetros

 _pSession_
  
> [entrada] Puntero a la sesión en uso por la aplicación cliente. 
    
 _cbEID_
  
> [entrada] Tamaño, en bytes, del identificador de entrada compuestos para estar separados. 
    
 _pEID_
  
> [entrada] Puntero al identificador de entrada compuestos a estar separados. 
    
 _pcbStoreEID_
  
> [out] Puntero al tamaño devuelto, en bytes, del identificador de entrada del almacén de mensajes que contiene el objeto. Si el parámetro _pEID_ señala a un identificador de entrada los, a continuación, el parámetro _pcbStoreEID_ apunta a un valor de cero. 
    
 _ppStoreEID_
  
> [out] Puntero a un puntero al identificador de entrada devuelto del almacén de mensajes que contiene el objeto. Si el parámetro _pEID_ señala a un identificador de entrada los, se devuelve NULL en el parámetro _ppStoreEID_ . 
    
 _pcbMsgEID_
  
> [out] Puntero al tamaño devuelto, en bytes, del identificador de entrada del objeto. Si el parámetro _pEID_ señala a un identificador de entrada los, el parámetro _pcbMsgEID_ es igual que el valor del parámetro _cbEID_ . 
    
 _ppMsgEID_
  
> [out] Puntero a un puntero al identificador de entrada devuelta del objeto. Si el parámetro _pEID_ señala a un identificador de entrada los, _ppMsgEID_ apunta a un puntero a una copia del identificador de entrada de los. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Si el identificador especificado por el parámetro _pEID_ es compuesto, se divide en el identificador de entrada del objeto dentro de su almacén de mensajes y el identificador de entrada de la tienda. Las cadenas de identificador de entrada los simplemente se copian. El identificador de compuestos para estar separados suele ser uno creado por la función [HrComposeEID](hrcomposeeid.md) . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Tras completar correctamente esta función, se libera la memoria que contiene el parámetro _pEID_ . La implementación de la llamada es responsable de liberar memoria para los parámetros de salida. 
  

