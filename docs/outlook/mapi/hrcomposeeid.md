---
title: HrComposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeEID
api_type:
- COM
ms.assetid: 8aba90d8-ea1f-4636-af80-17bfeadbdfa0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7de4fdefee67c79fb15ac28f821b015cdda6708d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429050"
---
# <a name="hrcomposeeid"></a>HrComposeEID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea un identificador de entrada compuesto para un objeto, normalmente un mensaje en un almacén de mensajes. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
HrComposeEID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  ULONG FAR * pcbEID,
  LPENTRYID FAR * ppEID
);
```

## <a name="parameters"></a>Parameters

 _psession_
  
> [in] Puntero a la sesión en uso por la aplicación cliente. 
    
 _cbStoreRecordKey_
  
> [in] Tamaño, en bytes, de la clave de registro del almacén de mensajes que contiene el mensaje u otro objeto. Si se pasa cero en el  _parámetro cbStoreRecordKey,_ el parámetro  _ppEID_ apunta a una copia del identificador de entrada del objeto. 
    
 _pStoreRecordKey_
  
> [in] Puntero a la clave de registro del almacén de mensajes que contiene el mensaje u otro objeto. 
    
 _cbMsgEID_
  
> [in] Tamaño, en bytes, del identificador de entrada del mensaje u otro objeto. 
    
 _pMsgEID_
  
> [in] Puntero al identificador de entrada del objeto. 
    
 _pcbEID_
  
> [salida] Puntero al tamaño, en bytes, del identificador devuelto. 
    
 _ppEID_
  
> [salida] Puntero a un puntero al identificador de entrada devuelto. Si el valor del parámetro  _cbStoreRecordKey_ es mayor que cero, el parámetro  _ppEID_ apunta a un puntero al identificador de entrada compuesto que se crea. Si  _cbStoreRecordKey_ es cero,  _ppEID_ apunta a un puntero a una copia del identificador de entrada del objeto. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Si el mensaje u otro objeto para el que se crea el identificador de entrada compuesta reside en un almacén de mensajes, el identificador se crea a partir del identificador de entrada del objeto y la clave de registro del almacén. Si el objeto no está en un almacén, es decir, si el número de bytes de la clave de registro de almacén pasada en  _cbStoreRecordKey_ es cero, el identificador de entrada del objeto simplemente se copia. 
  
La **función HrComposeEID** permite a las aplicaciones trabajar con objetos en varios almacenes mediante el uso de identificadores de entrada compuesta. Una aplicación puede llamar a [la función HrDecomposeEID](hrdecomposeeid.md) para dividir el identificador de entrada compuesta en sus constituyentes originales. 
  
## <a name="see-also"></a>Vea también



[HrComposeMsgID](hrcomposemsgid.md)
  
[HrDecomposeMsgID](hrdecomposemsgid.md)

