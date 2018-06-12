---
title: IProfAdmin IUnknown
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: c6192e6f92078f2f9bab0d55e9952d21ebb82af6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817890"
---
# <a name="iprofadmin--iunknown"></a>IProfAdmin: IUnknown

  
  
**Se aplica a**: Outlook 
  
Admite la administración de perfiles. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapix.h  <br/> |
|Expuestos por:  <br/> |Objeto de perfil de administración  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IProfAdmin  <br/> |
|Tipo de puntero:  <br/> |LPPROFADMIN  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[GetLastError](iprofadmin-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produjeron en un objeto de administración de perfiles.  <br/> |
|[GetProfileTable](iprofadmin-getprofiletable.md) <br/> |Proporciona acceso a la tabla de perfil, una tabla que contiene información acerca de todos los perfiles disponibles.  <br/> |
|[CreateProfile](iprofadmin-createprofile.md) <br/> |Crea un nuevo perfil.  <br/> |
|[DeleteProfile](iprofadmin-deleteprofile.md) <br/> |Elimina un perfil.  <br/> |
|[ChangeProfilePassword](iprofadmin-changeprofilepassword.md) <br/> |En desuso. Cambia la contraseña de un perfil.  <br/> |
|[CopyProfile](iprofadmin-copyprofile.md) <br/> |Copia un perfil.  <br/> |
|[RenameProfile](iprofadmin-renameprofile.md) <br/> |Asigna un nombre nuevo a un perfil.  <br/> |
|[SetDefaultProfile](iprofadmin-setdefaultprofile.md) <br/> |Establece o borra el perfil predeterminado de un cliente.  <br/> |
|[AdminServices](iprofadmin-adminservices.md) <br/> |Proporciona acceso a un objeto de administración del servicio de mensajes para realizar cambios en los servicios de mensaje en un perfil.  <br/> |
   
## <a name="see-also"></a>Ver también



[Interfaces MAPI](mapi-interfaces.md)

