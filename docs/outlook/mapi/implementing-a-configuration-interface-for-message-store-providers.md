---
title: Implementación de una interfaz de configuración para proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c349a03b0be465ed1262712372b6ee17a9812abd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415890"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a>Implementación de una interfaz de configuración para proveedores de almacenamiento de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de almacenamiento de mensajes son necesarios para implementar una interfaz que permita al usuario configurar el proveedor de almacén de mensajes para que se ejecute en el equipo del usuario. Normalmente, el proveedor de almacenamiento de mensajes se configura cuando el proveedor de almacenamiento de mensajes se agrega al perfil de un usuario. La interfaz de configuración del proveedor de almacenamiento de mensajes suele controlar tareas como la configuración de nombres de usuario y contraseñas para los almacenes de mensajes protegidos, la elección de rutas de archivos necesarios y la creación del mecanismo de almacenamiento subyacente que se va a usar, si es necesario.
  
Se obtiene acceso a la interfaz de configuración que implemente a través de puntos de entrada adicionales en la DLL del proveedor de servicios de mensajes. Para obtener más información, vea [configuración de un servicio de mensajes](configuring-a-message-service.md). La interfaz de configuración del proveedor de almacenamiento de mensajes es la única interfaz de usuario que debe implementar un proveedor de almacén de mensajes.
  
## <a name="see-also"></a>Ver también



[Caracter�sticas de almac�n de mensajes](message-store-features.md)

