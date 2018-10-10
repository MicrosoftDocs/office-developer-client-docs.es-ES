---
title: Habilitar una biblioteca DLL para que se ejecute en DCOM
TOCTitle: Enabling a DLL to Run on DCOM
ms:assetid: b405f767-91f0-c869-d34e-7a953de49106
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249859(v=office.15)
ms:contentKeyID: 48547211
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 26c83c9770ce7372338a054090025c67c32a9c36
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483898"
---
# <a name="enabling-a-dll-to-run-on-dcom"></a><span data-ttu-id="7f18e-102">Habilitar una biblioteca DLL para que se ejecute en DCOM</span><span class="sxs-lookup"><span data-stu-id="7f18e-102">Enabling a DLL to Run on DCOM</span></span>


<span data-ttu-id="7f18e-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f18e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7f18e-104">Los pasos siguientes describen cómo habilitar una biblioteca de vínculo dinámico (DLL) de un objeto de negocio de modo que pueda usar DCOM y Microsoft® Internet Information Services (HTTP) a través de Servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="7f18e-104">The following steps outline how to enable a business object dynamic-link libraries to use both DCOM and Microsoft® Internet Information Services (HTTP) via Component Services.</span></span>

1.  <span data-ttu-id="7f18e-p101">Cree un paquete vacío en el complemento MMC de Servicios de componentes. Utilizará el complemento MMC de Servicios de componentes para crear un paquete y agregar la biblioteca DLL a él. De este modo, se puede tener acceso a la .dll a través de DCOM, pero elimina la accesibilidad mediante IIS. (Si comprueba la dll en el Registro, verá que la clave **Inproc** ahora está vacía; al configurar el atributo Activation, explicado más adelante en este tema, se agrega un valor en la clave **Inproc**.)</span><span class="sxs-lookup"><span data-stu-id="7f18e-p101">Create a new empty package in the Component Services MMC snap-in. You will use the Component Services MMC snap-in to create a package and add the DLL into this package. This makes the .dll accessible through DCOM, but it removes the accessibility through IIS. (If you check in the registry for the .dll, the **Inproc** key is now empty; setting the Activation attribute, explained later in this topic, adds a value in the **Inproc** key.)</span></span>

2.  <span data-ttu-id="7f18e-p102">Instale un objeto de negocio en el paquete. O bien Importe el objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span><span class="sxs-lookup"><span data-stu-id="7f18e-p102">Install a business object into the package. -or- Import the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object into the package.</span></span>

3.  <span data-ttu-id="7f18e-p103">Establezca el atributo Activation del paquete en **En el proceso del creador** (aplicación de biblioteca). Para que se pueda tener acceso a la .dll mediante DCOM e IIS en el mismo equipo, debe establecer el atributo Activation del componente en el complemento MMC de Servicios de componentes. Después de establecer el atributo en **En el proceso del creador**, observará que se ha agregado una clave de servidor **Inproc** en el Registro que apunta a una .dll sustituta de los Servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="7f18e-p103">Set the Activation attribute for the package to **In the creator's process** (Library application). To make the .dll accessible through DCOM and IIS on the same computer, you must set the component's Activation attribute in the Component Services MMC snap-in. After you set the attribute to **In the creator's process**, you will notice that an **Inproc** server key in the registry has been added that points to a Component Services surrogate .dll.</span></span>
