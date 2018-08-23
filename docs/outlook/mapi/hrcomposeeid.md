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
ms.openlocfilehash: 335fac38ff3f084195a000ad32a27adcb85c1cc6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564818"
---
# <a name="hrcomposeeid"></a>HrComposeEID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea un identificador de entrada compuestos para un objeto, normalmente un mensaje en un almacén de mensajes. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
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

## <a name="parameters"></a>Parámetros

 _pSession_
  
> [entrada] Puntero a la sesión en uso por la aplicación cliente. 
    
 _cbStoreRecordKey_
  
> [entrada] Tamaño, en bytes, de la clave de registro del almacén de mensajes mantiene el mensaje u otro objeto. Si se pasa cero en el parámetro _cbStoreRecordKey_ , el parámetro _ppEID_ apunta a una copia del identificador de entrada del objeto. 
    
 _pStoreRecordKey_
  
> [entrada] Puntero a la clave de registro del almacén de mensajes que contiene el mensaje u otro objeto. 
    
 _cbMsgEID_
  
> [entrada] Tamaño, en bytes, del identificador de entrada del mensaje u otro objeto. 
    
 _pMsgEID_
  
> [entrada] Puntero al identificador de entrada del objeto. 
    
 _pcbEID_
  
> [out] Puntero al tamaño, en bytes, del identificador devuelto. 
    
 _ppEID_
  
> [out] Puntero a un puntero al identificador de la entrada devuelta. Si el valor del parámetro _cbStoreRecordKey_ es mayor que cero, el parámetro _ppEID_ apunta a un puntero al identificador de entrada compuestos que se crea. Si _cbStoreRecordKey_ es cero, _ppEID_ apunta a un puntero a una copia del identificador de entrada del objeto. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Si el mensaje u otro objeto para el que se está creando el identificador de entrada compuestos reside en un almacén de mensajes, se crea el identificador de identificador de entrada del objeto y la clave de registro de la tienda. Si el objeto no está en un almacén, es decir, si el número de bytes para la clave de registro de almacenamiento que se pasan en _cbStoreRecordKey_ es cero, el identificador del objeto entrada es simplemente se copian. 
  
La función **HrComposeEID** permite a las aplicaciones trabajar con objetos en varios almacenes mediante el uso de los identificadores de entrada compuestos. Una aplicación puede llamar a la función [HrDecomposeEID](hrdecomposeeid.md) para dividir el identificador de entrada compuesto en sus componentes originales. 
  
## <a name="see-also"></a>Recursos adicionales



[HrComposeMsgID](hrcomposemsgid.md)
  
[HrDecomposeMsgID](hrdecomposemsgid.md)

