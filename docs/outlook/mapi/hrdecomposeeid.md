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
ms.openlocfilehash: d3ef8b61b6042d9c3e715168d9131a74facef000
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436114"
---
# <a name="hrdecomposeeid"></a>HrDecomposeEID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Separa el identificador de entrada compuesto de un objeto, normalmente un mensaje en un almacén de mensajes, en el identificador de entrada de ese objeto en el almacén y en el identificador de entrada de la tienda.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
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

## <a name="parameters"></a>Parameters

 _psession_
  
> a Puntero a la sesión que usa la aplicación cliente. 
    
 _cbEID_
  
> a Tamaño, en bytes, del identificador de entrada compuesto que se va a separar. 
    
 _pEID_
  
> a Puntero al identificador de entrada compuesto que se va a separar. 
    
 _pcbStoreEID_
  
> contempla Puntero al tamaño devuelto, en bytes, del identificador de entrada del almacén de mensajes que contiene el objeto. Si el parámetro _pEID_ apunta a un identificador de entrada no compuesto, el parámetro _pcbStoreEID_ apunta a un valor de cero. 
    
 _ppStoreEID_
  
> contempla Puntero a un puntero al identificador de entrada devuelto del almacén de mensajes que contiene el objeto. Si el parámetro _pEID_ apunta a un identificador de entrada no compuesto, se devuelve null en el parámetro _ppStoreEID_ . 
    
 _pcbMsgEID_
  
> contempla Puntero al tamaño devuelto, en bytes, del identificador de entrada del objeto. Si el parámetro _pEID_ apunta a un identificador de entrada no compuesto, el parámetro _pcbMsgEID_ es igual al valor del parámetro _cbEID_ . 
    
 _ppMsgEID_
  
> contempla Puntero a un puntero al identificador de entrada devuelto del objeto. Si el parámetro _pEID_ apunta a un identificador de entrada no compuesto, _ppMsgEID_ apunta a un puntero a una copia del identificador de entrada no compuesto. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Si el identificador especificado por el parámetro _pEID_ es compuesto, se divide en el identificador de entrada del objeto dentro de su almacén de mensajes y el identificador de entrada del almacén. Simplemente se copian las cadenas del identificador de entrada no compuesto. El identificador compuesto que se va a separar suele ser uno de los creados por la función [HrComposeEID](hrcomposeeid.md) . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

La memoria que contiene el parámetro _pEID_ se publica tras la finalización correcta de esta función. La implementación de la llamada es responsable de liberar memoria para los parámetros de salida. 
  

