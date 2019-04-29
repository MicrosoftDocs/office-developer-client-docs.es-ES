---
title: IUnknown IProfAdmin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin
api_type:
- COM
ms.assetid: 274899cc-2894-4d99-84ec-f18121e856a0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cbdfba68490b1e756f277c6e552235368a86f310
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434119"
---
# <a name="iprofadmin--iunknown"></a>IProfAdmin : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Admite la administración de perfiles. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapix. h  <br/> |
|Expuesto por:  <br/> |Objeto de administración de perfiles  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IProfAdmin  <br/> |
|Tipo de puntero:  <br/> |LPPROFADMIN  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[Volvió](iprofadmin-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produjo en un objeto de administración de perfiles.  <br/> |
|[GetProfileTable](iprofadmin-getprofiletable.md) <br/> |Proporciona acceso a la tabla de perfiles, una tabla que contiene información sobre todos los perfiles disponibles.  <br/> |
|[CreateProfile](iprofadmin-createprofile.md) <br/> |Crea un nuevo perfil.  <br/> |
|[DeleteProfile](iprofadmin-deleteprofile.md) <br/> |Elimina un perfil.  <br/> |
|[ChangeProfilePassword](iprofadmin-changeprofilepassword.md) <br/> |En desuso. Cambia la contraseña de un perfil.  <br/> |
|[CopyProfile](iprofadmin-copyprofile.md) <br/> |Copia un perfil.  <br/> |
|[RenameProfile](iprofadmin-renameprofile.md) <br/> |Asigna un nombre nuevo a un perfil.  <br/> |
|[Setdefaultprofile a](iprofadmin-setdefaultprofile.md) <br/> |Establece o borra el perfil predeterminado de un cliente.  <br/> |
|[AdminServices](iprofadmin-adminservices.md) <br/> |Proporciona acceso a un objeto de administración del servicio de mensajes para realizar cambios en los servicios de mensajes de un perfil.  <br/> |
   
## <a name="see-also"></a>Ver también



[Interfaces MAPI](mapi-interfaces.md)

