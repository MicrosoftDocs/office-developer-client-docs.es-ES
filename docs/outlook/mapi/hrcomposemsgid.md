---
title: HrComposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeMsgID
api_type:
- COM
ms.assetid: bb76b147-6552-4cc4-920f-699170aea17f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3bcad4c236f71390f7a048eb66860720e9180e06
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582045"
---
# <a name="hrcomposemsgid"></a>HrComposeMsgID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una cadena de ASCII que representa un identificador de entrada compuestos para un objeto, normalmente un mensaje en un almacén de mensajes. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
HrComposeMsgID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  LPSTR FAR * pszMsgID
);
```

## <a name="parameters"></a>Parámetros

 _pSession_
  
> [entrada] Puntero a la sesión en uso por la aplicación cliente. 
    
 _cbStoreRecordKey_
  
> [entrada] Tamaño, en bytes, de la clave de registro del almacén de mensajes que contiene el mensaje u otro objeto. Si se pasa cero en el parámetro _cbStoreRecordKey_ , los puntos de parámetro _pszMsgID_ a una copia del identificador de entrada se convierten en texto. 
    
 _pStoreRecordKey_
  
> [entrada] Puntero a la clave de registro del almacén de mensajes que contiene el mensaje u otro objeto. 
    
 _cbMsgEID_
  
> [entrada] Tamaño, en bytes, del identificador de entrada del mensaje u otro objeto. 
    
 _pMsgEID_
  
> [entrada] Puntero al identificador de entrada del objeto. 
    
 _pszMsgID_
  
> [out] Puntero a la cadena devuelta de ASCII. Si el parámetro _cbStoreRecordKey_ es mayor que cero, los puntos de parámetro _pszMsgID_ a un identificador de entrada compuestos se convierten en texto. Si _cbStoreRecordKey_ es cero, _pszMsgID_ puntos a un identificador de entrada los convierten en texto. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Si el mensaje u otro objeto para el que se está creando el identificador de entrada compuestos reside en un almacén de mensajes, se crea la cadena de identificador de identificador de entrada del objeto y la clave de registro de la tienda. Si el objeto no está en un almacén, es decir, si el número de bytes de la clave de registro del almacén de pasa en el parámetro _cbStoreRecordKey_ es cero, el identificador del objeto entrada es simplemente copiado y convertir en una cadena. 
  
Llamar a la función **HrComposeMsgID** es equivalente a llamar a la función [HrComposeEID](hrcomposeeid.md) y, a continuación, la función [HrSzFromEntryID](hrszfromentryid.md) . 
  
 **HrComposeMsgID** permite que las aplicaciones de cliente trabajar con objetos en varios almacenes mediante el uso de los identificadores de entrada compuestos. Una aplicación puede llamar a la función [HrDecomposeMsgID](hrdecomposemsgid.md) para dividir el identificador de entrada compuesto en sus componentes originales. 
  

