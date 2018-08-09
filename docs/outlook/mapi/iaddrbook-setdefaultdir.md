---
title: IAddrBookSetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetDefaultDir
api_type:
- COM
ms.assetid: d5d60150-15e4-41ff-bfb0-0c67e2abcacc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 00d5b2bfc6b0c024f0ef12ce19fed90ef0af6721
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817133"
---
# <a name="iaddrbooksetdefaultdir"></a>IAddrBook::SetDefaultDir

  
  
**Hace referencia a**: Outlook 
  
Establece el contenedor especificado como el contenedor de la libreta de direcciones predeterminada.
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parámetros

 _cbEntryID_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada del contenedor de la libreta de direcciones predeterminada.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se estableció correctamente en el contenedor de la libreta de direcciones predeterminada.
    
## <a name="remarks"></a>Comentarios

Los clientes y proveedores de servicios de llamar al método **SetDefaultDir** para establecer un nuevo contenedor de libreta de direcciones predeterminada. El contenedor predeterminado es el contenedor que ve el usuario que se muestra en la libreta de direcciones cuando se abre por primera vez la libreta de direcciones. **SetDefaultDir** guarda el contenedor predeterminado como una entrada en el perfil. El contenedor permanece como el valor predeterminado hasta que se realiza otra llamada a **SetDefaultDir** en la misma sesión o en otra sesión, o se ha quitado el contenedor. 
  
> [!NOTE]
> La propiedad [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) corresponde a la opción **elija automáticamente** en el cuadro de diálogo Opciones de la libreta de direcciones. Cuando esta propiedad existe en la sección de perfil [IID_CAPONE_PROF](http://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) y se establece en **true**, el cuadro de diálogo de la libreta de direcciones ya no se establece de forma predeterminada en el contenedor especificado por **SetDefaultDir**, pero elige una libreta de direcciones que considera de Microsoft Outlook adecuada para el contexto en el que se muestra el cuadro de diálogo. Tenga en cuenta que esto puede producir una mala experiencia para los proveedores de libreta de direcciones de otros fabricantes. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|Abcontdlg.cpp  <br/> |CAbContDlg::OnSetDefaultDir  <br/> |MFCMAPI usa el método **SetDefaultDir** para realizar el contenedor de la libreta de direcciones especificado en el valor predeterminado uno.  <br/> |
   
## <a name="see-also"></a>Vea también



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[IMAPISession::Logoff](imapisession-logoff.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

