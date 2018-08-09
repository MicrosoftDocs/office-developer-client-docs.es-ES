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
ms.openlocfilehash: 423b03d674028a2f81b4c042d6e65e9acfb57274
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817829"
---
# <a name="initializing-the-transport-provider"></a>Inicializar el proveedor de transporte

  
  
**Hace referencia a**: Outlook 
  
La interfaz de transporte y cola de impresión define las llamadas que realiza la cola MAPI a un proveedor de transporte. Los proveedores de transporte implementan estas rutinas en una biblioteca de vínculos dinámicos (DLL). El primer punto de entrada directa en el archivo DLL utilizado por la cola MAPI debe ser la función de inicialización del proveedor de transporte [XPProviderInit](xpproviderinit.md).
  
MAPI utiliza la rutina **GetProcAddress** para obtener la dirección de la rutina de inicialización del proveedor de servicios y, a continuación, llama a esa rutina. El nombre de la rutina de inicialización es **XPProviderInit** para los proveedores de transporte. Es diferente de otros tipos de proveedores de servicios de MAPI para que una DLL puede contener cualquier combinación de tipos de proveedor de servicio, pero sólo un proveedor de servicios de un tipo determinado. Sin embargo, un proveedor de servicios de un determinado tipo puede implementar varios servicios de su tipo. Por ejemplo, un proveedor de transporte puede implementar la funcionalidad de transporte de mensajes a varios servicios de mensaje. 
  
El archivo de encabezado mapispi.h tiene una definición de tipo para el prototipo de función de la función de inicialización del proveedor de transporte y un nombre de procedimiento predefinidos para él. Exportar declaración en el archivo DLL de las rutinas de inicialización en los archivos de C y C++ de nomenclatura con los mismos nombres utilizados por **GetProcAddress** y mediante el uso de un sencillo. Archivo de definición, obtener automáticamente la comprobación de los parámetros en la rutina de inicialización de tipos. Vea el código de origen de proveedor de transporte de ejemplo para obtener ejemplos. Para obtener más información, vea [Ejemplo de proveedor de transporte](transport-provider-sample.md).
  
Si la llamada de inicialización de un proveedor de servicios se realiza correctamente pero no devuelve a un proveedor de servicios número de versión de la interfaz demasiado pequeño para MAPI controlar, MAPI inmediatamente llama al método de la **versión** del objeto de proveedor de servicio y continúa como si la inicialización de llamadas no se pudo tenía con MAPI_E_VERSION. De este modo MAPI y el proveedor de servicios conjuntamente definen el intervalo de números de versión del interfaz de proveedor de servicio que pueden controlar y, si nada coincide con, a continuación, cargar el proveedor de servicios se produce un error con un MAPI_E_VERSION devuelve valor. 
  
El último paso para la cola MAPI al obtener acceso a los recursos del proveedor de servicio es para iniciar sesión en el proveedor de transporte. La cola MAPI llama al método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) de la [IXPProvider: IUnknown](ixpprovideriunknown.md) objeto devuelto desde **XPProviderInit**. Se trata de la llamada donde se comprueban las credenciales, si se usa, y se permiten los cuadros de diálogo.
  
Si un proceso abre una segunda sesión de transporte en el mismo proveedor de transporte y la sesión MAPI, el archivo DLL del proveedor de transporte no debe crear un segundo objeto de proveedor. El primer objeto de proveedor debe usarse para iniciar sesión en la segunda sesión de transporte. Un proveedor de transporte debe programarse para admitir varias sesiones de transporte en un objeto de proveedor único. Sólo se debe crear un segundo objeto de proveedor si se usan diferentes sesiones MAPI en el mismo proceso.
  

