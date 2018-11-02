---
title: Implementar una interfaz de configuración para los proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 15833768fbd148ae4e689b5a80ed3479823864cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592930"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a>Implementar una interfaz de configuración para los proveedores de almacenamiento de mensajes

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de almacén de mensajes son necesarios para implementar una interfaz que permite al usuario configurar el proveedor de almacenamiento de mensajes para que se ejecute en el equipo del usuario. Normalmente, se configura el proveedor de almacén de mensajes cuando se agrega el proveedor de almacenamiento de mensajes a un perfil de usuario. Interfaz de configuración del proveedor de almacén de mensajes generalmente controla las tareas como la configuración de los nombres de usuario y contraseñas para almacenes de mensaje protegido, selección de rutas de acceso a los archivos necesarios, y crear el mecanismo de almacenamiento subyacente va a utilizar, si es necesario.
  
Se obtiene acceso a la interfaz de configuración que se implementa a través de puntos de entrada adicionales en el archivo DLL del proveedor de servicio mensaje. Para obtener más información, vea [configurar un servicio de mensajes](configuring-a-message-service.md). Interfaz de configuración del proveedor de almacén de mensajes es la única interfaz de usuario que debe implementar un proveedor de almacén de mensajes.
  
## <a name="see-also"></a>Vea también



[Caracter�sticas de almac�n de mensajes](message-store-features.md)

