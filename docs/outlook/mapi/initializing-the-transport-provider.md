---
title: Inicializar el proveedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 977c18ce-ece5-4ad1-ac97-5a680846ab83
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 474a8085ca8b82d11efd68c9fd4d8719fe239207
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416604"
---
# <a name="initializing-the-transport-provider"></a>Inicializar el proveedor de transporte

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La interfaz transport-spooler define las llamadas que la cola MAPI realiza a un proveedor de transporte. Los proveedores de transporte implementan estas rutinas en una biblioteca de vínculos dinámicos (DLL). El primer punto de entrada directo en la DLL usada por la cola MAPI debe ser la función de inicialización del proveedor de transporte [XPProviderInit](xpproviderinit.md).
  
MAPI usa la rutina **GetProcAddress para** obtener la dirección de la rutina de inicialización del proveedor de servicios y, a continuación, llama a esa rutina. El nombre de la rutina de inicialización **es XPProviderInit para** proveedores de transporte. Es diferente para otros tipos de proveedores de servicios MAPI, por lo que un DLL puede contener cualquier combinación de tipos de proveedor de servicios, pero solo un proveedor de servicios de un tipo determinado. Sin embargo, un proveedor de servicios de un tipo determinado puede implementar varios servicios de su tipo. Por ejemplo, un proveedor de transporte puede implementar la funcionalidad de transporte de mensajes en varios servicios de mensajes. 
  
El archivo de encabezado mapispi.h tiene una definición de tipo para el prototipo de función de la función de inicialización del proveedor de transporte y un nombre de procedimiento predefinido para ella. Al asignar un nombre a las rutinas de inicialización en los archivos C y C++ con los mismos nombres usados por **GetProcAddress** y mediante una declaración de exportación sencilla en el archivo DLL.DEF, obtiene automáticamente la comprobación de tipos de los parámetros de la rutina de inicialización. Vea el código fuente del proveedor de transporte de ejemplo para obtener ejemplos. Para obtener más información, vea [Transport Provider Sample](transport-provider-sample.md).
  
Si la llamada de inicialización de un proveedor de servicios se realiza correctamente pero devuelve un número de versión de interfaz de proveedor de servicios demasiado pequeño para que MAPI controle, MAPI llama inmediatamente al método **Release** del objeto del proveedor de servicios y procede como si la llamada de inicialización hubiera fallado con MAPI_E_VERSION. De este modo MAPI y el proveedor de servicios definen conjuntamente el intervalo de números de versión de la interfaz del proveedor de servicios que pueden controlar y, si nada coincide, la carga del proveedor de servicios falla con un MAPI_E_VERSION valor devuelto. 
  
El último paso para que la cola MAPI obtenga acceso a los recursos del proveedor de servicios es iniciar sesión en el proveedor de transporte. La cola MAPI llama al método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) del [objeto IXPProvider : IUnknown](ixpprovideriunknown.md) devuelto de **XPProviderInit**. Esta es la llamada donde se comprueban las credenciales, si se usan, y se pueden permitir cuadros de diálogo.
  
Si un proceso abre una segunda sesión de transporte en el mismo proveedor de transporte y sesión MAPI, el DLL del proveedor de transporte no debe crear un segundo objeto de proveedor. El primer objeto de proveedor debe usarse para iniciar sesión en la segunda sesión de transporte. Un proveedor de transporte debe programarse para admitir varias sesiones de transporte en un único objeto de proveedor. Solo se debe crear un segundo objeto de proveedor si se usan diferentes sesiones MAPI en el mismo proceso.
  

