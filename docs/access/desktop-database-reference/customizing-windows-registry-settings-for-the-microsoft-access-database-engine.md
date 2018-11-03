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
ms.openlocfilehash: 99e2b31cf686895a56e9d70b177314355c1aff3c
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945150"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a><span data-ttu-id="cc8ff-102">Personalización de la configuración del Registro de Windows para el motor de base de datos de Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="cc8ff-102">Customizing Windows registry settings for the Microsoft Access database engine</span></span>

<span data-ttu-id="cc8ff-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cc8ff-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cc8ff-104">Si su aplicación no funciona correctamente con funcionalidad predeterminada del motor de base de datos de Microsoft Access, puede que tenga que cambiar la configuración en el registro de Microsoft Windows que mejor se adapte a sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="cc8ff-104">If your application cannot work correctly with the default functionality of the Microsoft Access database engine, you may have to change the settings in the Microsoft Windows Registry to suit your needs.</span></span> <span data-ttu-id="cc8ff-105">El Registro de Windows también se puede utilizar para ajustar el funcionamiento del controlador ODBD e ISAM instalable.</span><span class="sxs-lookup"><span data-stu-id="cc8ff-105">The Windows Registry can also be used to tune the operation of the installable ISAM and ODBC driver.</span></span>

<span data-ttu-id="cc8ff-106">Puede personalizar la configuración del Registro de Windows de cuatro formas distintas:</span><span class="sxs-lookup"><span data-stu-id="cc8ff-106">You can customize the settings in the Windows Registry in four different ways:</span></span>

- <span data-ttu-id="cc8ff-107">[Use Regedit.exe para sobrescribir la configuración predeterminada](https://msdn.microsoft.com/library/ff193205\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="cc8ff-107">[Using Regedit.exe to overwrite the default settings](https://msdn.microsoft.com/library/ff193205\(v=office.15\))</span></span>
- <span data-ttu-id="cc8ff-108">[Creación de una parte en el árbol de registro de la aplicación para administrar la configuración](https://msdn.microsoft.com/library/ff836342\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="cc8ff-108">[Creating a portion in your application's registry tree to manage the settings](https://msdn.microsoft.com/library/ff836342\(v=office.15\))</span></span>
- <span data-ttu-id="cc8ff-109">[Mediante el método SetOption de DAO](https://msdn.microsoft.com/library/ff194471\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="cc8ff-109">[Using the SetOption method from DAO](https://msdn.microsoft.com/library/ff194471\(v=office.15\))</span></span>
- <span data-ttu-id="cc8ff-110">[Usar las propiedades de conexión en el proveedor Microsoft OLE DB para Access](https://msdn.microsoft.com/library/ff196356\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="cc8ff-110">[Using the Connection properties in the Microsoft OLE DB Provider for Access](https://msdn.microsoft.com/library/ff196356\(v=office.15\))</span></span>

