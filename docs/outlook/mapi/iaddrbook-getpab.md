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
ms.openlocfilehash: 1f93ee653c9365488432c4e797b171a199c30107
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583718"
---
# <a name="iaddrbookgetpab"></a>IAddrBook::GetPAB

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Devuelve el identificador de entrada del contenedor que se designa como la libreta de direcciones personales (PAB).
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parámetros

 _lpcbEntryID_
  
> [out] Un puntero para el número de bytes en el identificador de entrada indicado por el parámetro _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Un puntero a un puntero al identificador de entrada de la Libreta personal de direcciones. El parámetro _lppEntryID_ contiene cero si no se ha designado ningún contenedor como el archivo PAB. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El identificador de entrada de la Libreta personal de direcciones se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

Los clientes de llaman al método **GetPAB** para recuperar el identificador de entrada del contenedor designado como el archivo PAB. Si no se ha establecido una libreta personal de direcciones en el perfil, MAPI selecciona como el archivo PAB del primer contenedor en la jerarquía de la libreta de direcciones que permite que las modificaciones. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenPAB  <br/> |MFCMAPI usa el método **GetPAB** para obtener el identificador de la libreta de direcciones personales del usuario.  <br/> |
   
## <a name="see-also"></a>Vea también



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propiedad canónico PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

