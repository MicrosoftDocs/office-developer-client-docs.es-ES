---
title: IAddrBookGetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetPAB
api_type:
- COM
ms.assetid: 9830e09c-700f-469b-a54d-4e4e0583aa84
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6c565c088fd4ef7d5df141bf770c560f79535998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419901"
---
# <a name="iaddrbookgetpab"></a>IAddrBook::GetPAB

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve el identificador de entrada del contenedor designado como libreta de direcciones personal (PAB).
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parámetros

 _lpcbEntryID_
  
> [salida] Puntero al recuento de bytes en el identificador de entrada al que apunta el _parámetro lppEntryID._ 
    
 _lppEntryID_
  
> [salida] Puntero a un puntero al identificador de entrada del PAB. El  _parámetro lppEntryID_ contiene cero si no se ha designado ningún contenedor como PAB. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El identificador de entrada del PAB se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

Los clientes llaman **al método GetPAB** para recuperar el identificador de entrada del contenedor designado como PAB. Si no se ha establecido una PAB en el perfil, MAPI selecciona como PAB el primer contenedor de la jerarquía de libretas de direcciones que permite modificaciones. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenPAB  <br/> |MFCMAPI usa **el método GetPAB** para obtener el identificador de la libreta de direcciones personal del usuario.  <br/> |
   
## <a name="see-also"></a>Consulte también



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propiedad canónica PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

