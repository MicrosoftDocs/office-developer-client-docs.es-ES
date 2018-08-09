---
title: Mostrar las hojas de propiedades de configuración
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: aa3ddecbd5af56eef16f5ae3a349a027e689fc8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816693"
---
# <a name="displaying-configuration-property-sheets"></a>Mostrar las hojas de propiedades de configuración

**Hace referencia a**: Outlook 
  
Proveedores de transporte de utilizar el método [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) para implementar las hojas de propiedades de configuración. Cuando se llama a **DoConfigPropSheet**, el proveedor de transporte pasa un puntero a una matriz de propiedades junto con información sobre cómo mostrarlos. MAPI, a continuación, presenta las propiedades al usuario por medio de un cuadro de diálogo estándar. Se recomienda encarecidamente usar este mecanismo de hoja de propiedad al implementar el proveedor de transporte debido a la ventaja para el usuario de una interfaz coherente.
  
## <a name="transport-providers"></a>Proveedores de transporte

Los proveedores de transporte pueden usar la función [BuildDisplayTable](builddisplaytable.md) para simplificar la creación de una tabla para mostrar para su uso con **DoConfigPropSheet**. Los proveedores de transporte también pueden usar la API de la hoja de propiedad directamente. Tamaño de búfer de los cambios realizados en las propiedades, los proveedores de transporte, puede usar la función [CreateIProp](createiprop.md) . Esto simplifica el control de cancelaciones por el usuario, mientras que el usuario modifica los valores almacenados en las propiedades. Si es necesario, un proveedor de transporte también puede proporcionar un cuadro de diálogo Asistente para cuadro para simplificar las tareas de configuración para el usuario. 
  

