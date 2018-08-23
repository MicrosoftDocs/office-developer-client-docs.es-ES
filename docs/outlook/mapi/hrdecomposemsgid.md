---
title: HrDecomposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeMsgID
api_type:
- COM
ms.assetid: 5e6a9f3e-79be-4ffd-9d42-3a14cabb1435
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 828d7ebcbceead02441165e3af92ec7b47d9f001
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564629"
---
# <a name="hrdecomposemsgid"></a>HrDecomposeMsgID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Separa la representación ASCII del identificador de entrada compuesta de un objeto, normalmente un mensaje en un almacén de mensajes, en el identificador de entrada de ese objeto en el almacén y el identificador de entrada de la tienda. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
HrDecomposeMsgID(
  LPMAPISESSION psession,
  LPSTR szMsgID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a>Parámetros

 _pSession_
  
> [entrada] Puntero a la sesión en uso por la aplicación cliente. 
    
 _szMsgID_
  
> [entrada] La cadena que representa el identificador de entrada del objeto. 
    
 _pcbStoreEID_
  
> [out] Puntero al tamaño devuelto, en bytes, del identificador de entrada del almacén de mensajes que contiene el objeto. Si el parámetro _szMsgID_ apunta a un identificador de entrada de los de la cadena, a continuación, los puntos de parámetro _pcbStoreEID_ a cero. 
    
 _ppStoreEID_
  
> [out] Puntero a un puntero al identificador de entrada devuelto del almacén de mensajes que contiene el objeto. Si el parámetro _szMsgID_ señala a un identificador de entrada los, se devuelve NULL en el parámetro _ppStoreEID_ . 
    
 _pcbMsgEID_
  
> [out] Puntero al tamaño devuelto, en bytes, del identificador de entrada del objeto dentro de su almacén. Si el parámetro _szMsgID_ apunta a una cadena de identificador de entrada los, el parámetro _pcbMsgEID_ es igual que el valor del parámetro _cbEID_ . 
    
 _ppMsgEID_
  
> [out] Puntero a un puntero a la cadena de identificador de entrada devuelta del objeto dentro de su almacén. Si el parámetro _szMsgID_ señala a un identificador de entrada los, _ppMsgEID_ apunta a un puntero a una copia del identificador de entrada los convertida. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Si el identificador especificado por el parámetro _szMsgID_ es compuesto, es convertido a partir de ASCII y se dividen en el identificador de entrada del objeto dentro de su almacén de mensajes y el identificador de entrada de la tienda. Las cadenas de identificador de entrada los simplemente se convierten y copiadas. La cadena de identificador compuestos a estar separados suele ser uno creado por la función [HrComposeMsgID](hrcomposemsgid.md) . 
  
Llamar a la función **HrDecomposeMsgID** es equivalente a llamar a la función [HrEntryIDFromSz](hrentryidfromsz.md) y, a continuación, la función [HrDecomposeEID](hrdecomposeeid.md) . 
  

