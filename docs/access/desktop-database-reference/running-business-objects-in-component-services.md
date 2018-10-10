---
title: Ejecutar objetos de negocio en servicios de componentes
TOCTitle: Running Business Objects in Component Services
ms:assetid: 12103458-b1dd-10fc-37e8-883fd6c6b9d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248893(v=office.15)
ms:contentKeyID: 48543328
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41424fd62e915ecb2d54fdb49c939b788f458804
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484540"
---
# <a name="running-business-objects-in-component-services"></a><span data-ttu-id="32681-102">Ejecutar objetos de negocio en servicios de componentes</span><span class="sxs-lookup"><span data-stu-id="32681-102">Running Business Objects in Component Services</span></span>


<span data-ttu-id="32681-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="32681-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="32681-p101">Los objetos de negocio pueden ser archivos ejecutables (.exe) o bibliotecas de vínculo dinámico (.dll). La configuración que se usa para ejecutar el objeto de negocio depende de si el objeto es un archivo .dll o .exe:</span><span class="sxs-lookup"><span data-stu-id="32681-p101">Business objects can be executable files (.exe) or dynamic-link libraries (.dll). The configuration you use to run the business object depends on whether the object is a .dll or .exe file:</span></span>

  - <span data-ttu-id="32681-p102">Los objetos de negocio creados como archivos .exe se pueden llamar a través de DCOM. Si estos objetos de negocio se usan a través de Internet Information Services (IIS), estarán sometidos a un proceso adicional de cálculo de referencias de datos que ralentizará la actuación del cliente.</span><span class="sxs-lookup"><span data-stu-id="32681-p102">Business objects created as .exe files can be called through DCOM. If these business objects are used through Internet Information Services (IIS), they are subject to additional marshalingof data, which will slow client performance.</span></span>

  - <span data-ttu-id="32681-p103">Los objetos de negocio creados como archivos .dll se pueden utilizar por medio de IIS (y, por tanto, con HTTP). También se pueden utilizar sobre DCOM por medio de Servicios de componentes (o Microsoft Transaction Server, si está utilizando Windows NT). Los archivos DLL de objetos de negocio deberán registrarse en el equipo de servidor IIS para proporcionar accesibilidad a través de IIS. La sección "[Habilitar una biblioteca DLL para que se ejecute en DCOM](enabling-a-dll-to-run-on-dcom.md)" muestra los pasos necesarios para configurar una biblioteca DLL de modo que se ejecute en DCOM.</span><span class="sxs-lookup"><span data-stu-id="32681-p103">Business objects created as .dll files can be used via IIS (and therefore HTTP). They can also be used over DCOM only via Component Services (or Microsoft Transaction Server, if you are using Windows NT). Business object DLLs will need to be registered on the IIS server computer to give you accessibility via IIS. (For steps on how to configure a DLL to run on DCOM, see the section, "[Enabling a DLL to Run on DCOM](enabling-a-dll-to-run-on-dcom.md).")</span></span>


> [!NOTE]
> <P><span data-ttu-id="32681-112">Cuando los objetos de negocios en el nivel intermedio se implementan como componentes de servicios de componentes (mediante <STRONG>GetObjectContext</STRONG>, <STRONG>SetComplete</STRONG>y <STRONG>SetAbort</STRONG>), pueden usar servicios de componentes (o MTS, si está utilizando Windows NT) para los objetos de contexto mantener su estado entre diferentes llamadas de cliente.</span><span class="sxs-lookup"><span data-stu-id="32681-112">When business objects on the middle tier are implemented as Component Services components (using <STRONG>GetObjectContext</STRONG>, <STRONG>SetComplete</STRONG>, and <STRONG>SetAbort</STRONG>), they can use Component Services (or MTS, if you are using Windows NT) context objects to maintain their state across multiple client calls.</span></span> <span data-ttu-id="32681-113">Este escenario es posible con DCOM, que normalmente está implementado entre clientes y servidores de confianza (una intranet).</span><span class="sxs-lookup"><span data-stu-id="32681-113">This scenario is possible with DCOM, which is typically implemented between trusted clients and servers (an intranet).</span></span> <span data-ttu-id="32681-114">En este caso, el objeto <A href="dataspace-object-rds.md">RDS.DataSpace</A> y el método <A href="createobject-method-rds.md">CreateObject</A> del cliente se reemplazan con el objeto de contexto de transacción y el método <STRONG>CreateInstance</STRONG> (proporcionado por la interfaz <STRONG>ITransactionContext</STRONG> ), implementados por Servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="32681-114">In this case, the <A href="dataspace-object-rds.md">RDS.DataSpace</A> object and <A href="createobject-method-rds.md">CreateObject</A> method on the client side are replaced by the transaction context object and <STRONG>CreateInstance</STRONG> method (provided by the <STRONG>ITransactionContext</STRONG> interface), implemented by Component Services.</span></span></P>


