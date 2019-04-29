---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b9a31fec93ec7fafc4d1565d63e4bc427ba4050e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439110"
---
# <a name="hrgetgalfromemsmdbuid"></a>HrGetGALFromEmsmdbUID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve el identificador de entrada de la libreta de direcciones global para el servicio de Exchange identificado por _pEmsmdbUID_. El identificador de entrada devuelto debe liberarse mediante [MAPIFreeBuffer](mapifreebuffer.md).
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |abhelp. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a>Parameters

 _pSess_
  
> a La sesión iniciada en IMAPISession. No puede ser nulo.
    
 _pAddrBook_
  
> a La libreta de direcciones que se usa para abrir el identificador de entrada. No puede ser nulo.
    
 _pEmsmdbUID_
  
> a Un puntero a una **emsmdbUID** que identifica la GAL del servicio de Exchange que se va a recuperar. Si _pEmsmdbUID_ es null o el UID cero, esta función obtiene la GAL heredada del servicio de Exchange. 
    
 _lpcbeid_
  
> contempla Un puntero al número de bytes del identificador de entrada de la lista global de direcciones.
    
 _lppeid_
  
> contempla Un puntero al identificador de entrada de la lista global de direcciones. Debe liberarse con [MAPIFreeBuffer](mapifreebuffer.md).
    

