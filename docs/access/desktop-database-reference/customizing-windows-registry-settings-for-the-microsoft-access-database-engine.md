---
title: Personalización de la configuración del Registro de Windows para el motor de base de datos de Microsoft Access
TOCTitle: Customizing Windows registry settings for the Microsoft Access database engine
ms:assetid: ca7e958a-ea26-d67d-45b9-10aeb1eac96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834346(v=office.15)
ms:contentKeyID: 48547690
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032168
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7cbe8ad56e01249563f7b06c9018d923a96246e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295124"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a>Personalización de la configuración del Registro de Windows para el motor de base de datos de Microsoft Access

**Se aplica a:** Access 2013, Office 2013

Si la aplicación no funciona correctamente con la funcionalidad predeterminada del motor de base de datos de Microsoft Access, es posible que tenga que cambiar la configuración en el Registro de Microsoft Windows para que se adapte a sus necesidades. El Registro de Windows también se puede utilizar para ajustar el funcionamiento del controlador ODBD e ISAM instalable.

Puede personalizar la configuración del Registro de Windows de cuatro formas distintas:

- [Usar Regedit.exe para sobrescribir la configuración predeterminada](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-regedit-exe-to-overwrite-the-default-settings)
- [Crear una parte en el árbol del Registro de la aplicación para administrar la configuración](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/creating-a-portion-in-your-application-s-registry-tree-to-manage-the-settings)
- [Uso del método SetOption de DAO](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-setoption-method-from-dao)
- [Uso de las propiedades connection en el proveedor de Microsoft OLE DB para Access](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-connection-properties-in-the-microsoft-ole-db-provider-for-access)

