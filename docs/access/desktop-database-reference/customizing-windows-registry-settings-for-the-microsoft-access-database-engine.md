---
title: Personalizar la configuración del registro de Windows para el motor de base de datos de Microsoft Access
TOCTitle: Customizing Windows Registry Settings for the Microsoft Access Database Engine
ms:assetid: ca7e958a-ea26-d67d-45b9-10aeb1eac96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834346(v=office.15)
ms:contentKeyID: 48547690
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032168
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4a90981c936c933d2eadb191bbf0d2639cd8e641
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485931"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a><span data-ttu-id="9aaec-102">Personalizar la configuración del Registro de Windows para el motor de base de datos de Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="9aaec-102">Customizing Windows Registry Settings for the Microsoft Access Database Engine</span></span>


<span data-ttu-id="9aaec-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9aaec-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9aaec-p101">Si su aplicación no funciona correctamente con la funcionalidad predeterminada del motor de base de datos de Microsoft Access, es posible que necesite modificar la configuración del Registro de Microsoft® Windows® para que se ajuste a sus necesidades. El Registro de Windows también se puede utilizar para ajustar el funcionamiento del controlador ODBD e ISAM instalable.</span><span class="sxs-lookup"><span data-stu-id="9aaec-p101">If your application cannot work correctly with the default functionality of the Microsoft Access database engine, you may have to change the settings in the Microsoft® Windows® Registry to suit your needs. The Windows Registry can also be used to tune the operation of the installable ISAM and ODBC driver.</span></span>

<span data-ttu-id="9aaec-106">Puede personalizar la configuración del Registro de Windows de cuatro formas distintas:</span><span class="sxs-lookup"><span data-stu-id="9aaec-106">You can customize the settings in the Windows Registry in four different ways:</span></span>

<span data-ttu-id="9aaec-107">[Usar Regedit.exe para sobrescribir la configuración predeterminada](https://msdn.microsoft.com/library/ff193205\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="9aaec-107">[Using Regedit.exe to Overwrite the Default Settings](https://msdn.microsoft.com/library/ff193205\(v=office.15\))</span></span>

<span data-ttu-id="9aaec-108">[Crear una parte en el árbol del Registro de la aplicación para administrar la configuración](https://msdn.microsoft.com/library/ff836342\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="9aaec-108">[Creating a Portion in Your Application's Registry Tree to Manage the Settings](https://msdn.microsoft.com/library/ff836342\(v=office.15\))</span></span>

<span data-ttu-id="9aaec-109">[Usar el método SetOption de DAO](https://msdn.microsoft.com/library/ff194471\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="9aaec-109">[Using the SetOption Method from DAO](https://msdn.microsoft.com/library/ff194471\(v=office.15\))</span></span>

<span data-ttu-id="9aaec-110">[Usar las propiedades de conexión en el proveedor Microsoft OLE DB para Access](https://msdn.microsoft.com/library/ff196356\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="9aaec-110">[Using the Connection Properties in the Microsoft OLE DB Provider for Access](https://msdn.microsoft.com/library/ff196356\(v=office.15\))</span></span>

