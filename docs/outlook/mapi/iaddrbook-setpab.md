---
title: IAddrBookSetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetPAB
api_type:
- COM
ms.assetid: 75daf9d4-6975-435f-91e5-1b41e0047ab7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3f13a4d278b85ffae33e8f44f3a15eb499fb11b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817154"
---
# <a name="iaddrbooksetpab"></a>IAddrBook::SetPAB

  
  
**Hace referencia a**: Outlook 
  
Designa un contenedor determinado como la libreta de direcciones personales (PAB).
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parámetros

 _cbEntryID_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada del contenedor que se designarán como el archivo PAB. El parámetro _lpEntryID_ no puede ser NULL. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El contenedor especificado se ha establecido como el archivo PAB.
    
## <a name="remarks"></a>Comentarios

Los clientes y proveedores de servicios de llamar al método **SetPAB** para designar un contenedor determinado como el archivo PAB. El archivo PAB es un contenedor que consta de las entradas que se copió desde otros contenedores, así como las nuevas entradas. 
  
Una llamada a **SetPAB** establece un contenedor como el archivo PAB hasta que ese contenedor se realiza no está disponible o un contenedor nuevo se convierte en la Libreta personal de direcciones a través de una llamada posterior a **SetPAB**. 
  
Los clientes y proveedores no es necesario que llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para que el cambio PAB sea permanente. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|AbContDlg.cpp  <br/> |CAbContDlg::OnSetPAB  <br/> |MFCMAPI, utiliza el método **SetPAB** para realizar el contenedor especificado de la Libreta personal de direcciones.  <br/> |
   
## <a name="see-also"></a>Vea también



[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Propiedad canónica PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

