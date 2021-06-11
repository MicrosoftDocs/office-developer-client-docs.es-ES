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
ms.openlocfilehash: 29677ce74f405e8ca03f1639f3d98288532e9653
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424619"
---
# <a name="iaddrbooksetpab"></a>IAddrBook::SetPAB

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Designa un contenedor concreto como la libreta de direcciones personal (PAB).
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [in] Puntero al identificador de entrada del contenedor que se designará como PAB. El  _parámetro lpEntryID_ no puede ser NULL. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El contenedor especificado se ha establecido como PAB.
    
## <a name="remarks"></a>Comentarios

Los clientes y proveedores de servicios llaman al **método SetPAB** para designar un contenedor determinado como PAB. El PAB es un contenedor que consta de entradas copiadas de otros contenedores, así como entradas nuevas. 
  
Una llamada a **SetPAB** establece un contenedor como PAB hasta que dicho contenedor no está disponible o un nuevo contenedor se convierte en el PAB a través de una llamada posterior a **SetPAB**. 
  
Los clientes y proveedores no tienen que llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para que el cambio de PAB sea permanente. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|AbContDlg.cpp  <br/> |CAbContDlg::OnSetPAB  <br/> |MFCMAPI usa el **método SetPAB** para convertir el contenedor especificado en PAB.  <br/> |
   
## <a name="see-also"></a>Vea también



[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Propiedad canónica PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

