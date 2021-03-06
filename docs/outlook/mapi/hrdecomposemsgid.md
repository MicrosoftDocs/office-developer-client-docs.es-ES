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
ms.openlocfilehash: bff73ee5cf02680a2376106e21e0c743b995d336
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404438"
---
# <a name="hrdecomposemsgid"></a>HrDecomposeMsgID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Separa la representación ASCII del identificador de entrada compuesta de un objeto, normalmente un mensaje en un almacén de mensajes, en el identificador de entrada de ese objeto en el almacén y el identificador de entrada del almacén. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
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

## <a name="parameters"></a>Parameters

 _psession_
  
> [in] Puntero a la sesión en uso por la aplicación cliente. 
    
 _szMsgID_
  
> [in] Cadena que representa el identificador de entrada del objeto. 
    
 _pcbStoreEID_
  
> [salida] Puntero al tamaño devuelto, en bytes, del identificador de entrada del almacén de mensajes que contiene el objeto. Si el  _parámetro szMsgID_ apunta a una cadena de identificador de entrada no completa, el parámetro  _pcbStoreEID_ apunta a cero. 
    
 _ppStoreEID_
  
> [salida] Puntero a un puntero al identificador de entrada devuelto del almacén de mensajes que contiene el objeto. Si el _parámetro szMsgID_ apunta a un identificador de entrada no completo, null se devuelve en el _parámetro ppStoreEID._ 
    
 _pcbMsgEID_
  
> [salida] Puntero al tamaño devuelto, en bytes, del identificador de entrada del objeto dentro de su almacén. Si el _parámetro szMsgID_ apunta a una cadena de identificador de entrada no completa, el parámetro _pcbMsgEID_ es igual al valor del _parámetro cbEID._ 
    
 _ppMsgEID_
  
> [salida] Puntero a un puntero a la cadena de identificador de entrada devuelta del objeto dentro de su almacén. Si el  _parámetro szMsgID_ apunta a un identificador de entrada no completo,  _ppMsgEID_ apunta a un puntero a una copia convertida del identificador de entrada no completa. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Si el identificador especificado por el parámetro  _szMsgID_ es compuesto, se convierte desde ASCII y se divide en el identificador de entrada del objeto dentro de su almacén de mensajes y el identificador de entrada del almacén. Las cadenas de identificador de entrada no completa simplemente se convierten y copian. La cadena de identificador compuesto que se va a separar suele ser una creada por la [función HrComposeMsgID.](hrcomposemsgid.md) 
  
Llamar a **la función HrDecomposeMsgID** equivale a llamar a la [función HrEntryIDFromSz](hrentryidfromsz.md) y, a continuación, a la [función HrDecomposeEID.](hrdecomposeeid.md) 
  

