---
title: Folders
TOCTitle: Folders
ms:assetid: b72b5705-d77a-4cad-873d-457b9fb6553e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184634(v=office.15)
ms:contentKeyID: 55119856
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ecf342c54d1aa2020fbfad4175a220b2aefecbe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327185"
---
# <a name="folders"></a>Carpetas

En esta sección se proporcionan tareas de ejemplo relacionadas con las carpetas. Los objetos [Folders](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) representan la jerarquía de carpeta donde se almacenan los elementos de Microsoft Outlook. Algunos ejemplos de carpetas son las carpetas de Calendario, Correo y Elementos eliminados. En el ensamblado de interoperabilidad primario de Outlook (PIA), los miembros del objeto **Folder** se exponen como miembros del objeto [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)).

## <a name="in-this-section"></a>En esta sección

|Tema|Descripción|
|:----|:----------|
|[Agregar una carpeta a la lista de carpetas](how-to-add-a-folder-to-the-folder-list.md) |Usa el método [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) para agregar una carpeta a la lista de carpetas de Outlook.|
|[Enumerar carpetas](how-to-enumerate-folders.md)  |Enumera las carpetas mediante iteración por un conjunto de carpetas.|
|[Obtener una carpeta predeterminada y enumerar sus subcarpetas](how-to-get-a-default-folder-and-enumerate-its-subfolders.md) |Obtiene una carpeta predeterminada del almacén de usuario predeterminado y enumera sus subcarpetas.|
|[Obtener una carpeta con la ruta de acceso](how-to-get-a-folder-based-on-its-folder-path.md)  |Toma una ruta de acceso y obtiene la carpeta asociada.|
|[Seleccionar una carpeta y mostrar la información de la carpeta](how-to-select-a-folder-and-display-folder-information.md)  |Muestra información sobre una carpeta que un usuario selecciona desde una lista de la carpeta especificada mediante programación.|
|[Obtener la clase de mensaje predeterminada de una carpeta](how-to-get-the-default-message-class-of-a-folder.md)  |Usa la propiedad [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) para obtener la clase de mensaje predeterminada de una carpeta.|
|[Acceder a datos específicos a la solución almacenados como un mensaje oculto en una carpeta](how-to-access-solution-specific-data-stored-as-a-hidden-message-in-a-folder.md)  |Usa el objeto [StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) para recuperar datos almacenados como un mensaje oculto de una clase de mensaje específica de una carpeta.|
|[Asegurarse de que las propiedades personalizadas del elemento se admiten en las consultas de nivel de carpeta](how-to-ensure-that-custom-item-properties-are-supported-in-folder-level-queries.md) |Muestra cómo garantizar que al agregar una propiedad personalizada a un tipo de elemento también se agregue la propiedad a la carpeta, de modo que se pueda consultar esa propiedad personalizada en el nivel de carpetas.|

## <a name="see-also"></a>Vea también

- [Calendario](calendar.md)
- [Contactos](contacts.md)
- [Correo](mail.md)
- [How do I... (Outlook 2013 PIA reference)](how-do-i-outlook-2013-pia-reference.md) (¿Cómo se puede... [Referencia a PIA de Outlook 2013])

