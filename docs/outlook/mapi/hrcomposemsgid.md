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
ms.openlocfilehash: c035780d3d790d94551860a418401e63da1c2151
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424066"
---
# <a name="hrcomposemsgid"></a>HrComposeMsgID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una cadena ASCII que representa un identificador de entrada compuesto para un objeto, normalmente un mensaje en un almacén de mensajes. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
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

## <a name="parameters"></a>Parameters

 _psession_
  
> a Puntero a la sesión que usa la aplicación cliente. 
    
 _cbStoreRecordKey_
  
> a Tamaño, en bytes, de la clave de registro del almacén de mensajes que contiene el mensaje u otro objeto. Si se pasa cero en el parámetro _cbStoreRecordKey_ , el parámetro _pszMsgID_ apunta a una copia del identificador de entrada convertida en texto. 
    
 _pStoreRecordKey_
  
> a Puntero a la clave de registro del almacén de mensajes que contiene el mensaje u otro objeto. 
    
 _cbMsgEID_
  
> a Tamaño, en bytes, del identificador de entrada del mensaje u otro objeto. 
    
 _pMsgEID_
  
> a Puntero al identificador de entrada del objeto. 
    
 _pszMsgID_
  
> contempla Puntero a la cadena ASCII devuelta. Si el parámetro _cbStoreRecordKey_ es mayor que cero, el parámetro _pszMsgID_ apunta a un identificador de entrada compuesto convertido en texto. Si _cbStoreRecordKey_ es cero, _pszMsgID_ apunta a un identificador de entrada no compuesto convertido en texto. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Si el mensaje u otro objeto para el que se crea el identificador de entrada compuesto reside en un almacén de mensajes, la cadena de identificador se crea a partir del identificador de entrada del objeto y la clave de registro del almacén. Si el objeto no está en un almacén, es decir, si el número de bytes para la clave de registro de almacén que se pasa en el parámetro _cbStoreRecordKey_ es cero, el identificador de entrada del objeto simplemente se copia y se convierte en una cadena. 
  
Llamar a la función **HrComposeMsgID** equivale a llamar a la función [HrComposeEID](hrcomposeeid.md) y, a continuación, a la función [HrSzFromEntryID](hrszfromentryid.md) . 
  
 **HrComposeMsgID** permite a las aplicaciones cliente trabajar con objetos en varios almacenes a través del uso de identificadores de entrada compuesta. Una aplicación puede llamar a la función [HrDecomposeMsgID](hrdecomposemsgid.md) para dividir el identificador de entrada compuesta en sus componentes originales. 
  

