---
layout: blog
---

Click and drag nodes, scroll to zoom, and if you'd like to plan your backlog using our TMForum Open API dependency metadata underlying this visualization [get in touch with us](mailto:alex@ersatz.io) (alex@ersatz.io)!

<link href="http://visjs.org/dist/vis-network.min.css" rel="stylesheet" type="text/css"/>

<style type="text/css">
    #tmfdeps {
            /* width: 1900px;
            height: 400px;*/
            background-color:rgba(0, 0, 0, 0.5);
            /* border: 1px solid lightgray; */
    }
</style>

<div id="tmfdeps"></div>

<script type="text/javascript" src="http://visjs.org/dist/vis.js"></script>

<script type="text/javascript">
  // create an array with nodes
  var nodes = new vis.DataSet([
    {
      'id': '666',
      'label': 'TMF666 - Account Management API',
      'shape': 'box'
    },
    {
      'id': '640',
      'label': 'TMF640 - Activation and Configuration API',
      'shape': 'box'
    },
    {
      'id': '647',
      'label': 'TMF647 - Address API',
      'shape': 'box'
    },
    {
      'id': '651',
      'label': 'TMF651 - Agreement Management API',
      'shape': 'box'
    },
    {
      'id': '642',
      'label': 'TMF642 - Alarm Management API',
      'shape': 'box'
    },
    {
      'id': '646',
      'label': 'TMF646 - Appointment API',
      'shape': 'box'
    },
    {
      'id': '636',
      'label': 'TMF636 - Billing Management API',
      'shape': 'box'
    },
    {
      'id': '655',
      'label': 'TMF655 - Change Management API',
      'shape': 'box'
    },
    {
      'id': '681',
      'label': 'TMF681 - Communication API',
      'shape': 'box'
    },
    {
      'id': '678',
      'label': 'TMF678 - Customer Bill Management API',
      'shape': 'box'
    },
    {
      'id': '629',
      'label': 'TMF629 - Customer Management API',
      'shape': 'box'
    },
    {
      'id': '667',
      'label': 'TMF667 - Document Management API',
      'shape': 'box'
    },
    {
      'id': '662',
      'label': 'TMF662 - Entity Catalog Management API',
      'shape': 'box'
    },
    {
      'id': '673',
      'label': 'TMF673 - Geographic Address Management API',
      'shape': 'box'
    },
    {
      'id': '675',
      'label': 'TMF675 - Geographic Location Management API',
      'shape': 'box'
    },
    {
      'id': '674',
      'label': 'TMF674 - Geographic Site Management API',
      'shape': 'box'
    },
    {
      'id': '658',
      'label': 'TMF658 - Loyalty Management API',
      'shape': 'box'
    },
    {
      'id': '650',
      'label': 'TMF650 - Onboarding Management API',
      'shape': 'box'
    },
    {
      'id': '668',
      'label': 'TMF668 - Partnership Type Management API',
      'shape': 'box'
    },
    {
      'id': '632',
      'label': 'TMF632 - Party Management API',
      'shape': 'box'
    },
    {
      'id': '669',
      'label': 'TMF669 - Party Role Management API',
      'shape': 'box'
    },
    {
      'id': '676',
      'label': 'TMF676 - Payment Management API',
      'shape': 'box'
    },
    {
      'id': '670',
      'label': 'TMF670 - Payment Methods API',
      'shape': 'box'
    },
    {
      'id': '628',
      'label': 'TMF628 - Performance Management API',
      'shape': 'box'
    },
    {
      'id': '649',
      'label': 'TMF649 - Performance Management Threshold API',
      'shape': 'box'
    },
    {
      'id': '654',
      'label': 'TMF654 - Prepay Balance Management API',
      'shape': 'box'
    },
    {
      'id': '644',
      'label': 'TMF644 - Privacy Management API',
      'shape': 'box'
    },
    {
      'id': '620',
      'label': 'TMF620 - Product Catalog Management API',
      'shape': 'box'
    },
    {
      'id': '637',
      'label': 'TMF637 - Product Inventory Management API',
      'shape': 'box'
    },
    {
      'id': '679',
      'label': 'TMF679 - Product Offering Qualification API',
      'shape': 'box'
    },
    {
      'id': '622',
      'label': 'TMF622 - Product Ordering API',
      'shape': 'box'
    },
    {
      'id': '671',
      'label': 'TMF671 - Promotion API',
      'shape': 'box'
    },
    {
      'id': '648',
      'label': 'TMF648 - Quote Management API',
      'shape': 'box'
    },
    {
      'id': '680',
      'label': 'TMF680 - Recommendation API',
      'shape': 'box'
    },
    {
      'id': '634',
      'label': 'TMF634 - Resource Catalog Management API',
      'shape': 'box'
    },
    {
      'id': '664',
      'label': 'TMF664 - Resource Function Activation and Configuration API',
      'shape': 'box'
    },
    {
      'id': '639',
      'label': 'TMF639 - Resource Inventory Management API',
      'shape': 'box'
    },
    {
      'id': '652',
      'label': 'TMF652 - Resource Ordering Management API',
      'shape': 'box'
    },
    {
      'id': '623',
      'label': 'TMF623 - SLA Management API',
      'shape': 'box'
    },
    {
      'id': '633',
      'label': 'TMF633 - Service Catalog API',
      'shape': 'box'
    },
    {
      'id': '638',
      'label': 'TMF638 - Service Inventory Management API',
      'shape': 'box'
    },
    {
      'id': '641',
      'label': 'TMF641 - Service Ordering Management API',
      'shape': 'box'
    },
    {
      'id': '656',
      'label': 'TMF656 - Service Problem Management API (SPM)',
      'shape': 'box'
    },
    {
      'id': '645',
      'label': 'TMF645 - Service Qualification API',
      'shape': 'box'
    },
    {
      'id': '657',
      'label': 'TMF657 - Service Quality Management API',
      'shape': 'box'
    },
    {
      'id': '653',
      'label': 'TMF653 - Service Test Management API',
      'shape': 'box'
    },
    {
      'id': '684',
      'label': 'TMF684 - Shipment Tracking API',
      'shape': 'box'
    },
    {
      'id': '663',
      'label': 'TMF663 - Shopping Cart API',
      'shape': 'box'
    },
    {
      'id': '621',
      'label': 'TMF621 - Trouble Ticket API',
      'shape': 'box'
    },
    {
      'id': '677',
      'label': 'TMF677 - Usage Consumption Management API',
      'shape': 'box'
    },
    {
      'id': '635',
      'label': 'TMF635 - Usage Management API',
      'shape': 'box'
    },
    {
      'id': '672',
      'label': 'TMF672 - User Roles and Permissions API',
      'shape': 'box'
    }
  ])
  // create an array with edges
  var edges = new vis.DataSet([
    {
      'from': '666',
      'to': '650',
      'arrows': 'to'
    },
    {
      'from': '666',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '666',
      'to': '670',
      'arrows': 'to'
    },
    {
      'from': '640',
      'to': '638',
      'arrows': 'to'
    },
    {
      'from': '640',
      'to': '633',
      'arrows': 'to'
    },
    {
      'from': '640',
      'to': '639',
      'arrows': 'to'
    },
    {
      'from': '640',
      'to': '634',
      'arrows': 'to'
    },
    {
      'from': '640',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '651',
      'to': '620',
      'arrows': 'to'
    },
    {
      'from': '651',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '651',
      'to': '667',
      'arrows': 'to'
    },
    {
      'from': '646',
      'to': '647',
      'arrows': 'to'
    },
    {
      'from': '646',
      'to': '667',
      'arrows': 'to'
    },
    {
      'from': '646',
      'to': '629',
      'arrows': 'to'
    },
    {
      'from': '646',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '646',
      'to': '622',
      'arrows': 'to'
    },
    {
      'from': '646',
      'to': '621',
      'arrows': 'to'
    },
    {
      'from': '636',
      'to': '629',
      'arrows': 'to'
    },
    {
      'from': '636',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '655',
      'to': '623',
      'arrows': 'to'
    },
    {
      'from': '655',
      'to': '638',
      'arrows': 'to'
    },
    {
      'from': '655',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '655',
      'to': '667',
      'arrows': 'to'
    },
    {
      'from': '681',
      'to': '667',
      'arrows': 'to'
    },
    {
      'from': '681',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '678',
      'to': '667',
      'arrows': 'to'
    },
    {
      'from': '678',
      'to': '636',
      'arrows': 'to'
    },
    {
      'from': '678',
      'to': '666',
      'arrows': 'to'
    },
    {
      'from': '678',
      'to': '670',
      'arrows': 'to'
    },
    {
      'from': '678',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '629',
      'to': '666',
      'arrows': 'to'
    },
    {
      'from': '629',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '629',
      'to': '650',
      'arrows': 'to'
    },
    {
      'from': '629',
      'to': '670',
      'arrows': 'to'
    },
    {
      'from': '667',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '667',
      'to': '629',
      'arrows': 'to'
    },
    {
      'from': '662',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '662',
      'to': '667',
      'arrows': 'to'
    },
    {
      'from': '674',
      'to': '647',
      'arrows': 'to'
    },
    {
      'from': '674',
      'to': '675',
      'arrows': 'to'
    },
    {
      'from': '674',
      'to': '673',
      'arrows': 'to'
    },
    {
      'from': '674',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '650',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '650',
      'to': '651',
      'arrows': 'to'
    },
    {
      'from': '650',
      'to': '666',
      'arrows': 'to'
    },
    {
      'from': '668',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '668',
      'to': '651',
      'arrows': 'to'
    },
    {
      'from': '668',
      'to': '666',
      'arrows': 'to'
    },
    {
      'from': '668',
      'to': '669',
      'arrows': 'to'
    },
    {
      'from': '669',
      'to': '666',
      'arrows': 'to'
    },
    {
      'from': '669',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '669',
      'to': '670',
      'arrows': 'to'
    },
    {
      'from': '669',
      'to': '650',
      'arrows': 'to'
    },
    {
      'from': '676',
      'to': '666',
      'arrows': 'to'
    },
    {
      'from': '676',
      'to': '629',
      'arrows': 'to'
    },
    {
      'from': '676',
      'to': '636',
      'arrows': 'to'
    },
    {
      'from': '676',
      'to': '678',
      'arrows': 'to'
    },
    {
      'from': '676',
      'to': '620',
      'arrows': 'to'
    },
    {
      'from': '676',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '676',
      'to': '652',
      'arrows': 'to'
    },
    {
      'from': '676',
      'to': '622',
      'arrows': 'to'
    },
    {
      'from': '676',
      'to': '641',
      'arrows': 'to'
    },
    {
      'from': '670',
      'to': '666',
      'arrows': 'to'
    },
    {
      'from': '670',
      'to': '629',
      'arrows': 'to'
    },
    {
      'from': '670',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '670',
      'to': '658',
      'arrows': 'to'
    },
    {
      'from': '654',
      'to': '666',
      'arrows': 'to'
    },
    {
      'from': '654',
      'to': '637',
      'arrows': 'to'
    },
    {
      'from': '654',
      'to': '639',
      'arrows': 'to'
    },
    {
      'from': '654',
      'to': '620',
      'arrows': 'to'
    },
    {
      'from': '654',
      'to': '670',
      'arrows': 'to'
    },
    {
      'from': '654',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '644',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '644',
      'to': '620',
      'arrows': 'to'
    },
    {
      'from': '620',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '620',
      'to': '650',
      'arrows': 'to'
    },
    {
      'from': '620',
      'to': '667',
      'arrows': 'to'
    },
    {
      'from': '620',
      'to': '623',
      'arrows': 'to'
    },
    {
      'from': '620',
      'to': '633',
      'arrows': 'to'
    },
    {
      'from': '620',
      'to': '668',
      'arrows': 'to'
    },
    {
      'from': '637',
      'to': '650',
      'arrows': 'to'
    },
    {
      'from': '637',
      'to': '668',
      'arrows': 'to'
    },
    {
      'from': '637',
      'to': '636',
      'arrows': 'to'
    },
    {
      'from': '637',
      'to': '620',
      'arrows': 'to'
    },
    {
      'from': '637',
      'to': '633',
      'arrows': 'to'
    },
    {
      'from': '637',
      'to': '651',
      'arrows': 'to'
    },
    {
      'from': '637',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '679',
      'to': '620',
      'arrows': 'to'
    },
    {
      'from': '679',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '622',
      'to': '650',
      'arrows': 'to'
    },
    {
      'from': '622',
      'to': '668',
      'arrows': 'to'
    },
    {
      'from': '622',
      'to': '636',
      'arrows': 'to'
    },
    {
      'from': '622',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '622',
      'to': '637',
      'arrows': 'to'
    },
    {
      'from': '622',
      'to': '629',
      'arrows': 'to'
    },
    {
      'from': '622',
      'to': '679',
      'arrows': 'to'
    },
    {
      'from': '622',
      'to': '620',
      'arrows': 'to'
    },
    {
      'from': '648',
      'to': '636',
      'arrows': 'to'
    },
    {
      'from': '648',
      'to': '650',
      'arrows': 'to'
    },
    {
      'from': '648',
      'to': '651',
      'arrows': 'to'
    },
    {
      'from': '648',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '648',
      'to': '667',
      'arrows': 'to'
    },
    {
      'from': '648',
      'to': '646',
      'arrows': 'to'
    },
    {
      'from': '648',
      'to': '637',
      'arrows': 'to'
    },
    {
      'from': '648',
      'to': '622',
      'arrows': 'to'
    },
    {
      'from': '648',
      'to': '620',
      'arrows': 'to'
    },
    {
      'from': '680',
      'to': '637',
      'arrows': 'to'
    },
    {
      'from': '680',
      'to': '620',
      'arrows': 'to'
    },
    {
      'from': '680',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '634',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '634',
      'to': '667',
      'arrows': 'to'
    },
    {
      'from': '634',
      'to': '675',
      'arrows': 'to'
    },
    {
      'from': '634',
      'to': '647',
      'arrows': 'to'
    },
    {
      'from': '664',
      'to': '675',
      'arrows': 'to'
    },
    {
      'from': '664',
      'to': '647',
      'arrows': 'to'
    },
    {
      'from': '664',
      'to': '634',
      'arrows': 'to'
    },
    {
      'from': '664',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '639',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '639',
      'to': '667',
      'arrows': 'to'
    },
    {
      'from': '639',
      'to': '634',
      'arrows': 'to'
    },
    {
      'from': '639',
      'to': '647',
      'arrows': 'to'
    },
    {
      'from': '639',
      'to': '675',
      'arrows': 'to'
    },
    {
      'from': '652',
      'to': '646',
      'arrows': 'to'
    },
    {
      'from': '652',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '652',
      'to': '647',
      'arrows': 'to'
    },
    {
      'from': '652',
      'to': '675',
      'arrows': 'to'
    },
    {
      'from': '652',
      'to': '634',
      'arrows': 'to'
    },
    {
      'from': '652',
      'to': '639',
      'arrows': 'to'
    },
    {
      'from': '633',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '633',
      'to': '667',
      'arrows': 'to'
    },
    {
      'from': '638',
      'to': '633',
      'arrows': 'to'
    },
    {
      'from': '638',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '638',
      'to': '622',
      'arrows': 'to'
    },
    {
      'from': '638',
      'to': '639',
      'arrows': 'to'
    },
    {
      'from': '638',
      'to': '637',
      'arrows': 'to'
    },
    {
      'from': '638',
      'to': '641',
      'arrows': 'to'
    },
    {
      'from': '641',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '641',
      'to': '633',
      'arrows': 'to'
    },
    {
      'from': '641',
      'to': '639',
      'arrows': 'to'
    },
    {
      'from': '641',
      'to': '637',
      'arrows': 'to'
    },
    {
      'from': '641',
      'to': '638',
      'arrows': 'to'
    },
    {
      'from': '641',
      'to': '646',
      'arrows': 'to'
    },
    {
      'from': '641',
      'to': '622',
      'arrows': 'to'
    },
    {
      'from': '641',
      'to': '641',
      'arrows': 'to'
    },
    {
      'from': '641',
      'to': '652',
      'arrows': 'to'
    },
    {
      'from': '656',
      'to': '621',
      'arrows': 'to'
    },
    {
      'from': '656',
      'to': '638',
      'arrows': 'to'
    },
    {
      'from': '656',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '656',
      'to': '639',
      'arrows': 'to'
    },
    {
      'from': '656',
      'to': '675',
      'arrows': 'to'
    },
    {
      'from': '656',
      'to': '647',
      'arrows': 'to'
    },
    {
      'from': '656',
      'to': '642',
      'arrows': 'to'
    },
    {
      'from': '656',
      'to': '623',
      'arrows': 'to'
    },
    {
      'from': '656',
      'to': '637',
      'arrows': 'to'
    },
    {
      'from': '645',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '645',
      'to': '633',
      'arrows': 'to'
    },
    {
      'from': '657',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '657',
      'to': '633',
      'arrows': 'to'
    },
    {
      'from': '657',
      'to': '673',
      'arrows': 'to'
    },
    {
      'from': '653',
      'to': '633',
      'arrows': 'to'
    },
    {
      'from': '653',
      'to': '638',
      'arrows': 'to'
    },
    {
      'from': '684',
      'to': '622',
      'arrows': 'to'
    },
    {
      'from': '663',
      'to': '641',
      'arrows': 'to'
    },
    {
      'from': '663',
      'to': '622',
      'arrows': 'to'
    },
    {
      'from': '663',
      'to': '652',
      'arrows': 'to'
    },
    {
      'from': '663',
      'to': '673',
      'arrows': 'to'
    },
    {
      'from': '663',
      'to': '675',
      'arrows': 'to'
    },
    {
      'from': '621',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '621',
      'to': '636',
      'arrows': 'to'
    },
    {
      'from': '621',
      'to': '629',
      'arrows': 'to'
    },
    {
      'from': '677',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '677',
      'to': '639',
      'arrows': 'to'
    },
    {
      'from': '635',
      'to': '632',
      'arrows': 'to'
    },
    {
      'from': '635',
      'to': '620',
      'arrows': 'to'
    },
    {
      'from': '672',
      'to': '632',
      'arrows': 'to'
    }
  ])
  // create a network
  var container = document.getElementById('tmfdeps')
  var data = {
    nodes: nodes,
    edges: edges
  }
  var options = {}
  var network = new vis.Network(container, data, options)
</script>
